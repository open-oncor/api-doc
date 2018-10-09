### Регистрация заболевания пациента (java)

### ![POST](../../../../img/post.png) [/ehr/add](../index.md)

```java
public class AddEhr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Patients.EHR ehr = client.addEHR(Patients.EHR.newBuilder()
                .setPatientId(patient.getId())
                .build());
        
        String id = ehr.getId();
        Diagnosis.ShortDz dz = ehr.getDz();
    }
}
```
