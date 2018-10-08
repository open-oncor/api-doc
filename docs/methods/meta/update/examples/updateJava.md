[Работа с метаданными](../index.md)

### ![POST](../../../../img/post.png) [/meta/update](../index.md)

### Java пример

```java
public class QueryUpdate {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();
        final Meta.Update.Builder updateBuilder = Meta.Update.newBuilder();

        final List<Meta.Object> objects = getObjects();

        objects.forEach(o -> {
            final Meta.Update.Statment.Builder statement = Meta.Update.Statment.newBuilder();
            statement.setObjectId(o.getId());
            final String entryNameTest = "U:" + apiUser + ":exp";
            final Meta.Object.Entry newEntry = o.getMetaList().stream()
                    .filter(entry -> Objects.equals(entryNameTest, entry.getName())).findFirst()
                    .orElseGet(() -> Meta.Object.Entry.newBuilder()
                            .setName(entryNameTest)
                            .setInt64(0)
                            .build());
            if (newEntry.getInt64() < 2) {
                statement.setAction(Meta.Update.Action.SET);
                statement.addMeta(newEntry.toBuilder().setInt64(newEntry.getInt64() + 1).build());
            } else {
                statement.setAction(Meta.Update.Action.REMOVE);
            }
            updateBuilder.addStatement(statement);
        });

        client.updateMeta(updateBuilder.build());
    }
}
```

**[HTTP пример](update.md)**