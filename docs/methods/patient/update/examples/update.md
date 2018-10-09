### Изменение данных пациента (http)

### ![POST](../../../../img/post.png) [/patient/update](../index.md)

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

