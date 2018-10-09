### Пример добавления записи RcChem (java)

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

```java
public class AddRcChem {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcChem(Records.Rc.RcChem.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Directories.ChemKind.newBuilder().setCode("NONE"))
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .addDrugs(Directories.DrugRecord.newBuilder()
                                .setDrug(Directories.Drug.newBuilder().setCode("Э001"))
                                .setUnit(Directories.DoseUnit.newBuilder().setCode("MKG"))
                                .setDose(123.0)
                        )
                        .addSrv(Directories.Srv59Chem.newBuilder().setCode("SRV_4_1_1"))
                )
                .build()
        );

        String id = newEhrRecord.getId();
        Records.Rc.RcChem rcChem = newEhrRecord.getRcChem();
    }
}

```
