[Работа с пациентами](../../../../index.md)
=====================================

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

### Java пример

```java
public class AddRcClinicalGroup {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcClinicalGroup(Records.Rc.RcClinicalGroup.newBuilder()
                        .setGroupType(Directories.ClinicalGroupType.newBuilder().setCode("NONE"))
                )
                .build());

        Records.Rc.RcClinicalGroup rcClinicalGroup = rc.getRcClinicalGroup();
        Directories.ClinicalGroupType groupType = rcClinicalGroup.getGroupType();
    }
}

```

**[HTTP примеры](add.md)**