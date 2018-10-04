[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcAppointmentQuery](../index.md)

### Примеры

**Request**

POST `http://tempurl.com/search/start/RcAppointmentQuery HTTP/1.1`
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