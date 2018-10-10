### Добавление медицинской записи пациенту (записи общие для пациента, не относящиеся ни к одному из заболеваний)

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

```java
public class AddRcRegIn {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcRegIn(Records.Rc.RcRegIn.newBuilder()
                        .setClause(Directories.RegInClause.newBuilder().setCode("NONE")))
                .build());

        Records.Rc.RcRegIn rcRegIn = rc.getRcRegIn();
        Directories.RegInClause clause = rcRegIn.getClause();
    }
}
```

