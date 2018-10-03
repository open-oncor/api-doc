# [Сценарии](../index.md)

## Постановка на учёт пациента в ОНКОР

1. [/patient/add](../../methods/patient/add/examples/add.md) `добавление нового пациента в ОНКОР` или
 [/patient/search](../../methods/patient/search/examples/search.md) `поиск пациента в ОНКОР`
2. [/ehr/add](../../methods/ehr/add/examples/add.md) `добавление ЭМЗ пациента`
3. [/ehr/record/add](../../methods/ehr/record/add/examples/add.md) `добавление записи в ЭМЗ`

```java
class NewPatientRcDz {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        client.getLocMetTypeDirectory();

        final Patients.Patient newPatient = client.addPatient(Patients.Patient.newBuilder()
                .setFirstName("RcDzTest")
                .setMiddleName(new Date().toString())
                .setLastName("Test")
                .build());

        final Patients.EHR newEhr = client.addEHR(Patients.EHR.newBuilder()
                .setPatientId(newPatient.getId())
                .build());

        client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(newPatient.getId())
                .setEhrId(newEhr.getId())
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
                .build());

    }
}
```