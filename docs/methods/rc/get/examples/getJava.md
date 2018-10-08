[Работа с медицинскими записями](../index.md)
===============================

### ![GET](../../../../img/get.png) [/rc/get`?id={id}`](../index.md)

### Java пример

```java
public class GetRc {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Records.Rc rc = client.getRc("1577:16819");
        String id = rc.getId();
        String patientId = rc.getPatientId();
    }
}
```

**[HTTP пример](get.md)**