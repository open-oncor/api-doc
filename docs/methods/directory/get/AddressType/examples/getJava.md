[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/Gender](../index.md)

### Java пример

```java
public class GetAddressTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> addressTypes = client.getAddressTypes();
        Directories.AddressType addressType = addressTypes.get(0);

        String id = addressType.getId();
        String caption = addressType.getCaption();
    }
}

```

**[HTTP пример](get.md)**