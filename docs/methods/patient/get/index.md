## Получение данных пациента по его ключу

### ![GET](../../../img/get.png) /patient/get`?id={patient_id}`
* **URL parameter:** [id](../../../types/types.md#com.siams.med.api.Patient)
* **Response:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]

В ответе передаётся массив с единственным объектом - [Patient](../../../types/types.md#com.siams.med.api.Patient).



### Пример http

**Request:** 

GET `http://dev.onco-reg.ru/api/1.0/json/patient/get?id=65:33650 HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

**Response:**

```json
{
    "result":[
        {
            "id":"#70:33669",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "last_name":"Иванов",
            "birth_day":"1901-01-01",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ010101М",
            "ehr_count":0,
            "company_name":"",
            "snils":"",
            "phones":"+7 911"
        }
    ]
}
```
