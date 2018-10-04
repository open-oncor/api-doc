[Работа с пациентами](../index.md)
==================================

### ![GET](../../../../img/get.png) [/patient/get`?id={patient_id}`](../index.md)

### Примеры

**Request:** GET `http://localhost:8080/api/1.0/json/patient/get?id=65:33650 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "id":"#65:33650",
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