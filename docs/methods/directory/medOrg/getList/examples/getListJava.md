[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/medOrg/getList](../index.md)

### Java пример

```java
public class GetMedOrgList {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.MedOrg> medOrgs = client.getMedOrgs();
        Directories.MedOrg medOrg = medOrgs.get(0);

        String id = medOrg.getId();
        String unq = medOrg.getUnq();
    }
}

```

**[HTTP примеры](getList.md)**