[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/BloodType](../index.md)

```java
public class GetBloodTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.BloodType> bloodTypes = client.getBloodTypes();
        Directories.BloodType bloodType = bloodTypes.get(0);

        String id = bloodType.getId();
        String caption = bloodType.getCaption();
    }
}
```

**[HTTP примеры](get.md)**