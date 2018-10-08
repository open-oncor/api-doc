[Работа с метаданными](../index.md)
===================================

### ![POST](../../../../img/post.png) [/meta/query](../index.md)

### Java пример

```java
public class MetaQuery {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();
        final Meta.Query.Builder queryBuilder = Meta.Query.newBuilder();

        final List<Meta.Object> objects = client.queryMeta(queryBuilder
                .addIds("65:902")
                .addIds("66:18041")
                .build());

        Meta.Object object = objects.get(0);
        String id = object.getId();
        Meta.Object.Entry meta = object.getMeta(0);
    }
}
```

**[HTTP примеры](query.md)**