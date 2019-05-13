## Поиск пациентов
### ![GET](../../../img/get.png) /patient/search`?name=Иванов%20Иван%20Иванович&dob=311288&gender=M&limit=20`
* **URL parameter: name=last_name%20first_name%20middle_name&dob(date of birth)=311288&gender=M&limit=20**
* **Response:** [[PatientSearchResult](../../../types/types.md#com.siams.med.api.PatientSearchResult)]
* **Response:`422`**

Возвращает массив пациентов в соответствии с запросом или пустой массив, если не найдено ни одного пациента. 

### Пример http

**Request:** 

GET `http://dev.onco-reg.ru/api/1.0/json/patient/search?name=Иванов%20Иван%20Иванович&dob=311288&gender=M&limit=20 HTTP/1.1`

**Response `200`**

```json
{
    "patient_query":{
        "last_name":"Иванов",
        "first_name":"Иван",
        "middle_name":"Иванович",
        "birth_day":"1967-12-03"
    }
}
```

**Response `422`**
```json
{
    "error":{
        "name":"InvalidArgumentsException",
        "message":"Invalid patient name",
        "uuid":"d2eaae0f-274b-4254-8b69-163c2c3a6143"
    }
}
```

### Пример java

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