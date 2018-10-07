# [Сценарии](../index.md)

## Регистрация нового пациента в ОНКОР

Для того, чтобы зарегистрировать нового пациента, необходимо проверить наличие пациента в ОНКОР используя [/patient/search](../../methods/patient/search/index.md).
Если пациент найден и требуется добавить нового, то нужно использовать безусловное добавление пациента 
[/patient/forceAdd](../../methods/patient/forceAdd/index.md).
В случае, если пациент не найден, добавить пациента в ОНКОР можно при помощи [/patient/add](../../methods/patient/add/index.md).

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
        } else {
            client.forceAddPatient(patientToAdd);   
        }
    }
}
```