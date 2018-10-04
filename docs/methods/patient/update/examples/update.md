[Работа с пациентами](../../index.md)
=====================================

[Работа с пациентами](../index.md)
==================================

### ![POST](../../../../img/post.png) [/patient/update](../index.md)

**Request**

POST `http://tempurl.com/patient/update HTTP/1.1`

```json
{
    "patient_update":{
        "id":"65:33650",
        "code":"ИИИ",
        "entry":[
            {
                "snils":"Тестовый СНИЛС"
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
            "snils":"Тестовый СНИЛС",
            "phones":"+7 911"
        }
    ]
}
```