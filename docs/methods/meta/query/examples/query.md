[Работа с метаданными](../index.md)
===================================

### ![POST](../../../../img/post.png) [/meta/query](../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/meta/query HTTP/1.1`
```json
{
    "query":{
        "ids":[
            "#65:33650",
            "#69:17722",
            "#66:21901",
            "#69:21247",
            "#70:29967"
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
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":1
                }
            ]
        },
        {
            "id":"#69:17722",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":1
                }
            ]
        },
        {
            "id":"#66:21901",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":1
                }
            ]
        },
        {
            "id":"#69:21247",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":1
                }
            ]
        },
        {
            "id":"#70:29967",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":1
                }
            ]
        }
    ]
}
```

**[Java пример](queryJava.md)**

