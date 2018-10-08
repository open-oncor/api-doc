[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/get/RecordsPage](../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/get/RecordsPage HTTP/1.1`
```json
{
    "page":{
        "job":{
            "id":"43153f0a-9865-4943-a856-c30449d4eb0e"
        },
        "offset":0,
        "size":5
    }
}
```

**Response**

```json
{
    "result":[
        {
            "page":{
                "job":{
                    "id":"43153f0a-9865-4943-a856-c30449d4eb0e"
                },
                "offset":0,
                "size":5
            }
        }
    ]
}
```

**[Java пример](RecordsPageJava.md)**