[Работа со справочниками](../../../index.md)
===========================================

### ![GET](../../../../../img/get.png) [/directory/get/DrPrsG](../index.md)

### Java пример

```java
public class GetPrsG {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.DrPrsG> genders = client.getGenders();
        Directories.DrPrsG drPrsG = genders.get(0);

        String id = drPrsG.getId();
        String caption = drPrsG.getCaption();
    }
}
```

**[HTTP примеры](get.md)**