[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcDocQuery](../index.md)

### Examples

**URI** POST `http://tempurl.com/search/start/RcDocQuery HTTP/1.1`

**Request**

```json
{
    "query":{
        "from_date":"2018-01-01"
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"6921ac85-0e80-4b87-a1b5-66c817bb69b3"
        }
    ]
}
```