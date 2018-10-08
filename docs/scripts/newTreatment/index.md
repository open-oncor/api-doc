# [Сценарии](../index.md)

## Выгрузка данных проведенного лечения из МИС МО в ОНКОР

Для выгрузки данных проведённого лечения необходим пациент 
([Регистрация пацианта в ОНКОР](../newPatient/index.md) или [Поиск пациента](../../methods/patient/search/index.md)). 
После получения пациента требуется получить список заболеваний пациента, найти в нём необходимое, затем добавить 
в него запись [/ehr/record/add](../../methods/ehr/record/add/examples/RcDz/add.md). Если необходимое заболевание не 
найдено, то его требуется добавить [/ehr/add](../../methods/ehr/add/examples/add.md).

**Java пример добавления записи RcRay**
```java
public class NewRcRay {
    public static void main(String[] args) throws IOException {
            final ProtoBuffClient client = newProtoBuffClient();
    
            final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
    
            Patients.Patient patient = Patients.Patient.newBuilder()
                    .setFirstName("Иван")
                    .setMiddleName("Иванович")
                    .setLastName("Иванов")
                    .setBirthDay("1901-01-01")
                    .setPhones("+7 911")
                    .setGender(Directories.DrPrsG.newBuilder()
                            .setId("1")
                            .build())
                    .build();
    
            List patients = client.searchPatients(Patients.PatientQuery.newBuilder()
                    .setCode(patient.getCode())
                    .build());
    
            if (patients.isEmpty()) {
                client.addPatient(patient);
            } else {
                client.forceAddPatient(patient);
            }
    
            Records.Rc ehrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                    .setPatientId(patient.getId())
                    .setEhrId(patient.getId())
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
    
            client.addEhrRecord(Records.Rc.newBuilder()
                    .setPatientId(ehrRecord.getPatientId())
                    .setEhrId(ehrRecord.getEhrId())
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
        }
}

```