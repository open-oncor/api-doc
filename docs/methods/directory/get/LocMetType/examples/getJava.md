[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/LocMetType](../index.md)

### Java пример

```java
public class GetLocMetTypeDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.LocMetType> locMetTypeDirectory = client.getLocMetTypeDirectory();
        Directories.LocMetType locMetType = locMetTypeDirectory.get(0);

        String caption = locMetType.getCaption();
        Directories.LocMet.Code code = locMetType.getCode();
    }
}
```

**[HTTP примеры](get.md)**