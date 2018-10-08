[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/DrNK0439](../index.md)

### Java пример

```java
public class GetDrNK0465 {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.DrNK0439> drNK0439Directory = client.getDrNK0439Directory();
        Directories.DrNK0439 drNK0439 = drNK0439Directory.get(0);

        String id = drNK0439.getId();
        String caption = drNK0439.getCaption();
    }
}

```

[### HTTP примеры](get.md)