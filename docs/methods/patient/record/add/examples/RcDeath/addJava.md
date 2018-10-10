### Добавление статистической записи ‘Регистрация смерти’ (RcDeath) указанному пациенту (java)

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

```java
public class AddRcDeath {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcDeath(Records.Rc.RcDeath.newBuilder()
                        .setReason(Directories.RBiMKB308.newBuilder().setCode("C50")))
                .build());

        Records.Rc.RcDeath RcDeath = rc.getRcDeath();
    }
}
```

