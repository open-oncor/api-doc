[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcReferralQuery](../index.md)

### Examples

**URI** POST `http://tempurl.com/search/start/RcReferralQuery HTTP/1.1`

**Request**

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
            "id":"c3f5422c-3450-4b5f-bb12-f51f35729b89"
        }
    ]
}
```