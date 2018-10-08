[Работа с заболеваниями пациента](../../index.md)
==============================

### ![GET](../../../../img/get.png) [/ehr/getList`?patient_id={patient_id}`](../index.md)

### Java пример

```java
public class GetEhrList {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient;

        List<Patients.EHR> ehrList = client.getEHRList(patient.getId());
        Patients.EHR ehr = ehrList.get(0);

        String id = ehr.getId();
        Diagnosis.ShortDz dz = ehr.getDz();
    }
}
```

**[HTTP примеры](getList.md)**