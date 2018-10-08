[Работа с заболеваниями пациента](../../../../index.md)
=================================

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Java пример

```java
public class AddRcOper {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        final Patients.Patient patient = getPatient();
        final Patients.EHR ehr = getEhr();
        final ProtoBuffClient client = newProtoBuffClient();
        final Directories.DrNK0439 compl = getDr();
        final Directories.Srv59Oper srv = getSrv();
        final Directories.MedOrg medOrg = getMedOrg();

        Records.Rc newEhrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setEhrId(ehr.getId())
                .setRcOper(Records.Rc.RcOper
                        .newBuilder()
                        .setOperation(Directories.DrNK0465.newBuilder().setId("845").build())
                        .setCondition(Directories.TherapyCond.newBuilder().setId("1").build())
                        .setOrgUnitId(medOrg.getOrgUnitId())
                        .setIntraCompl(compl)
                        .setAfterCompl(compl)
                        .addSrv(srv)
                        .build())
                .build());

        String id = newEhrRecord.getId();
        Records.Rc.RcOper rcOper = newEhrRecord.getRcOper();
    }
}
```

**[HTTP примеры](add.md)**