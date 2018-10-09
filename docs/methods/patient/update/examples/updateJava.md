Изменение данных пациента (java)
=

### ![POST](../../../../img/post.png) [/patient/update](../index.md)

```java
public class UpdatePatient {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = client.updatePatient(Patients.PatientUpdate.newBuilder()
                .setId("70:33669")
                .setCode("ИИИ")
                .addEntry(
                        Patients.PatientUpdate.Entry.newBuilder()
                                .setSnils("Пример снилса")
                                .build()
                )
                .build()
        );

        String snils = patient.getSnils();
    }
}
```

