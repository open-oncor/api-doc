### Пример добавления записи RcReferral (java)

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

```java
public class AddRcReferral {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = rcDzTest.client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrRecord.getPatientId())
                .setEhrId(ehrRecord.getEhrId())
                .setRcReferral(Records.Rc.RcReferral.newBuilder()
                        .setPurpose("Цель направления")
                        .setRoutingList(Routing.RoutingList.newBuilder()
                                .setAdmissionDate("2018-02-01")
                                .setApplyFirstDate("2018-02-01")
                                .setApplyLastDate("2018-02-01")
                                .setApplyLastOnAnyOtherDiseaseDate("2018-02-01")
                                .setRequestDate("2018-02-01")
                                .setExaminationLsatDate("2018-02-01")
                                .setTreatmentFirstDate("2018-02-01")
                                .setExpertOpinionDate("2018-02-01")
                                .setExpertOpinion("Экспертное заключение")
                                .addDiagnostics(Routing.RoutingList.Diagnostics.newBuilder()
                                        .setType(Directories.DiagnosticsType.newBuilder().setCode("OAM"))
                                        .setDate("2018-01-01")
                                        .setNote("Примечание к обследованию"))
                                .setNote("Примечание к направлению")
                        )
                )
                .build()
        );

    }
}

```
