### Пример добавления записи RcHorm (java)

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Java пример

```java
public class AddRcHorm {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcHorm(Records.Rc.RcHorm.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Records.Rc.RcHorm.Kind.newBuilder().setXrt(true))
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .addDrugs(Directories.DrugRecord.newBuilder()
                                .setDrug(Directories.Drug.newBuilder().setCode("Ю001"))
                                .setUnit(Directories.DoseUnit.newBuilder().setCode("MKG"))
                                .setDose(123.0)
                        )
                )
                .build()
        );

        String id = newRecord.getId();
        Records.Rc.RcHorm rcHorm = newRecord.getRcHorm();
    }
}

```