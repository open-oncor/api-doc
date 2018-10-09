### Пример добавления записи RcRay (java)

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

```java
public class AddRcRay {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        final ProtoBuffClient client = newProtoBuffClient();
        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcRay(Records.Rc.RcRay.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Directories.RayKind.newBuilder().setCode("NONE"))
                        .setMethod(Directories.RayMethod.newBuilder().setCode("NONE"))
                        .setWay(Directories.RayWay.newBuilder().setCode("NONE"))
                        .setRadio(Directories.RayRadio.newBuilder().setCode("NONE"))
                        .setDoze(1f)
                        .setDozeMeta(1f)
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .setSessionCount(1)
                        .addSrv(Directories.Srv59Ray.newBuilder().setCode("SRV_3_1_1"))
                )
                .build()
        );

        String id = newEhrRecord.getId();
        Records.Rc.RcRay rcRay = newEhrRecord.getRcRay();
    }
}
```
