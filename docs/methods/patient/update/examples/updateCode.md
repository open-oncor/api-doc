[Работа с пациентами](../index.md)
=====================================

### ![POST](../../../../img/post.png) [/patient/update](../index.md)

```java
public class UpdatePatient {
    public static void main(String[] args) throws IOException {
        newProtoBuffClient()
                .updatePatient(Patients.PatientUpdate.newBuilder()
                        .addEntry(
                                Patients.PatientUpdate.Entry.newBuilder()
                                        .setSnils("Тестовый снилс")
                                        .build()
                        )
                        .build()
                );
    }
}
```

**[HTTP примеры](update.md)**