[Работа с пациентами](../../index.md)
=====================================

### ![POST](../../../../img/post.png) [/patient/search](../../search/index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/search HTTP/1.1`
```json
{
    "patient_query":{
        "first_name":"Иванов",
        "middle_name":"Иван",
        "last_name":"Иванович",
        "birth_day":"1944-06-14"
    }
}
```

**Response `200`**
```json
{
    "result":[
        {
            "id":"#70:33669",
            "first_name":"Иванов",
            "middle_name":"Иван",
            "last_name":"Иванович",
            "birth_day":"1944-06-14",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ140644М",
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

**[Java пример](searchJava.md)**