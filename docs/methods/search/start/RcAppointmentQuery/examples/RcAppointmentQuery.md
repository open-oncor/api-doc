[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcAppointmentQuery](../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcAppointmentQuery HTTP/1.1`
```json
{
    "query":{
        "from_date":"2017-10-01",
        "to_date":"2017-12-10"
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"cebb037d-9902-405a-995c-5345ca045fc4"
        }
    ]
}
```

**[Java пример](RcAppointmentQueryJava.md)**