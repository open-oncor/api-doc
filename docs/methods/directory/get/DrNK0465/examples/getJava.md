[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/DrNK0465](../index.md)

### Java пример

```java
public class GetDrNK0439 {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.DrNK0465> drNK0465Directory = client.getDrNK0465Directory();
        Directories.DrNK0465 drNK0465 = drNK0465Directory.get(0);

        String id = drNK0465.getId();
        String caption = drNK0465.getCaption();
    }
}

```

[### HTTP примеры](get.md)