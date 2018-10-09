Поиск пациентов (java)
=

### ![POST](../../../../img/post.png) [/patient/search](../../search/index.md)

```java
class SearchPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        //Поиск по коду ИИИ
        for (Patients.Patient patient : client.searchPatients(Patients.PatientQuery
                .newBuilder()
                .setCode("ИИИ")
                .build())) {
        }

        //Поиск по коду ИИИ290878")
        for (Patients.Patient patient : client.searchPatients(Patients.PatientQuery
                .newBuilder()
                .setCode("ИИИ290878")
                .build())) {
        }

        //Поиск по коду ИИИ + Gender"
        for (Patients.Patient patient : client.searchPatients(Patients.PatientQuery
                .newBuilder()
                .setCode("ИИИ")
                .setGender(Directories.DrPrsG.newBuilder().setId("2"))
                .build())) {
        }

        //"Поиск по имени")
        for (Patients.Patient patient : client.searchPatients(Patients.PatientQuery
                .newBuilder()
                .setFirstName("Иван ")
                .setMiddleName(" ИванОвич")
                .setLastName("ИвАнов  ")
                .setGender(Directories.DrPrsG.newBuilder().setId("1"))
                .build())) {
        }

    }
}
```
