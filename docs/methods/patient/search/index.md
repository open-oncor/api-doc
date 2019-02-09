## Поиск пациентов

### ![POST](../../../img/post.png) /patient/search
* **Request:** [PatientQuery](../../../types/types.md#com.siams.med.api.PatientQuery) **patient_query** <first_name, last_name, middle_name, birth_day>
* **Response:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]

Возвращает массив пациентов в соответствии с запросом или пустой массив, если не найдено ни одного пациента. 


### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/search HTTP/1.1`
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

**Response `200`**
```json
{
    "result":[
        {
            "id":"#70:33669",
            "last_name":"Иванов",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "birth_day":"1967-12-03",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ031267М",
            "ehr_count":1,
            "company_name":"",
            "snils":"",
            "address":{
                "address":"",
                "federal_code":"",
                "region_code":"",
                "town":" Каменск-Уральский",
                "street":"",
                "house":"",
                "flat":"",
                "postal_code":"",
                "fias":"",
                "kladr":"",
                "okato":"",
                "med_terr_unq":"1.2.643.2.75.1.100.2.66.660800",
                "living_area_type":{
                    "id":"1"
                }
            }
        }
    ]
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
