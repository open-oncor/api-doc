[Работа с пациентами](../../index.md)
=====================================

### ![POST](../../../../img/post.png) [/patient/add](../index.md)

### Примеры

**Request**

POST `http://tempurl.com/patient/add HTTP/1.1`

```json
{
    "patient":{
        "first_name":"Иван",
        "middle_name":"Иванович",
        "last_name":"Иванов",
        "birth_day":"1901-01-01",
        "gender":{
            "id":"1"
        },
        "phones":"+7 911"
    }
}
```

**Response `200`**

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

**Response `422`**

```json
{
    "error":{
        "name":"com.siams.med.api.InvalidArgumentsException",
        "message":"Invalid patient name",
        "uuid":"16bfee9a-2616-4a58-85c2-9ba4ac782cf4"
    }
}
```