[Работа с заболеваниями пациента](../../../../index.md)
=================================

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Java пример

```java
public class AddRcDz {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();
        
        Patients.Patient patient = getPatient();
        Patients.EHR ehr = getEhr();

        Records.Rc ehrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setEhrId(ehr.getId())
                .setRcDz(Records.Rc.RcDz.newBuilder()
                        .setDiagnosis(Diagnosis.Dz.newBuilder()
                                .setIcd10(Directories.RBiMKB308.newBuilder().setCode("C50"))
                                .setStatus(Directories.DrDzSt.newBuilder().setId("1"))
                                .setPrimacy(Directories.DrDzPr.newBuilder().setId("1"))
                                .setMorphClass(Directories.RBiNK0366.newBuilder().setCode("8001/3"))
                                .setTumorMain(Directories.DrDzTM.newBuilder().setId("-1"))
                                .setTumorSide(Directories.DrDzTS.newBuilder().setId("4"))
                                .setHowDiscover(Directories.DrDzHD.newBuilder().setId("0"))
                                .setMethod(Directories.DrDzMthd.newBuilder().setId("0"))
                                .setPlural(Directories.DrDzPl.newBuilder().setId("0"))
                                .setResAutopsy(Directories.DrDzRA.newBuilder().setId("0"))
                                .setWhyOld(Directories.DrDzWO.newBuilder().setId("10"))
                                .setLocMet(Directories.LocMet.newBuilder()
                                        .addCodes(Directories.LocMet.Code.UNKNOWN)
                                        .addCodes(Directories.LocMet.Code.OTHER_ORGANS)
                                )
                                .setTnm(Diagnosis.TNM.newBuilder()
                                        .setT(Directories.TnmT.newBuilder().setCode("T_X"))
                                        .setN(Directories.TnmN.newBuilder().setCode("N_X"))
                                        .setM(Directories.TnmM.newBuilder().setCode("M_X"))
                                        .setG(Directories.TnmG.newBuilder().setCode("G_X"))
                                )
                                .setStage(Directories.DzStage.newBuilder().setCode("NA"))
                        )
                )
                .build()
        );

        String id = ehrRecord.getId();
        Records.Rc.RcDz rcDz = ehrRecord.getRcDz();
    }
}

```

**[HTTP пример](add.md)**