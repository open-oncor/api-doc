[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/TherapyCond](../index.md)

### Java пример

```java
public class GetTherapyCondDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.TherapyCond> therapyCondDirectory = client.getTherapyCondDirectory();
        Directories.TherapyCond therapyCond = therapyCondDirectory.get(0);

        String id = therapyCond.getId();
        String caption = therapyCond.getCaption();
    }
}

```

**[HTTP примеры](get.md)**