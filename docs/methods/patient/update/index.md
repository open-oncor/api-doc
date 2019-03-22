## Изменение данных пациента

### ![POST](../../../img/post.png) /patient/update
* **Request:** [PatientUpdate](../../../types/types.md#com.siams.med.api.PatientUpdate) **patient <id, code>**
* **Response:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/update HTTP/1.1`

```json
{
    "patient_update":{
        "id":"70:33669",
        "code":"ИИИ010154",
        "entry":[
            {
                "snils":"Пример снилса"
            }
        ]
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#70:33669",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "last_name":"Иванов",
            "birth_day":"1954-01-01",
            "code":"ИИИ010154",
            "ehr_count":1,
            "company_name":"",
            "snils":"Пример снилса"
        }
    ]
}
```


### Пример java

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

