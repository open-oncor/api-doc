[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcReferralQuery](../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcReferralQuery HTTP/1.1`
```json
{
    "query":{
        "has_appointment":false,
        "from_date":"2017-10-01",
        "to_date":"2019-12-10"
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"a8a10778-dc14-41cc-ac97-4db300fa99a4"
        }
    ]
}
```

**[Java пример](RcReferralQueryJava.md)**