[Работа с медицинскими записями](../index.md)
===============================

### ![GET](../../../../img/get.png) [/rc/getList`?ehr_id={ehr_id}`](../index.md)

### Java пример

```java
public class GetList {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Records.Rc> rcList = client.getRcList("1054:29080");

        Records.Rc rc = rcList.get(0);

        String id = rc.getId();
        String patientId = rc.getPatientId();
    }
}
```

**[HTTP пример](getList.md)**