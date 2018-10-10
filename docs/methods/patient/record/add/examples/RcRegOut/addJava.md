### Добавление статистической записи 'Снятие с учёта' (RcRegOut) указанному пациенту (java)

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

### Java пример

```java
public class AddRcRegOut {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcRegOut(Records.Rc.RcRegOut.newBuilder()
                        .setReason(Directories.RegOutReason.newBuilder().setCode("NONE")))
                .build());

        Records.Rc.RcRegOut rcRegOut = rc.getRcRegOut();
        Directories.RegOutReason reason = rcRegOut.getReason();
    }
}
```
