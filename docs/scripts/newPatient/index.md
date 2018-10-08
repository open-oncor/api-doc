# [Сценарии](../index.md)

## Регистрация пациента

Для того, чтобы зарегистрировать нового пациента, сначала необходимо проверить наличие такого пациента используя [/patient/search](../../methods/patient/search/index.md) - возможно такой пациент уже есть. В случае, если пациент не найден, добавить пациента можно при помощи [/patient/add](../../methods/patient/add/index.md).

```java
class AddPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patientToAdd = Patients.Patient.newBuilder()
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
                .setCode(patientToAdd.getCode())
                .build());

        if(patients.isEmpty()){
            client.addPatient(patientToAdd);
        }
    }
}
```