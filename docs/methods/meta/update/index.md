## Изменение метаданных для медицинской записи

### ![POST](../../../img/post.png) /meta/update
* **Request:** [Update](../../../types/types.md#com.siams.med.api.Update) 
* **Response:** [[Meta.proto](../../../types/types.md#metaproto)]

Обновляет метаданные [Meta.proto](../../../types/types.md#metaproto)

**Пример http**

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/meta/update HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`


```json
{
    "update":{
        "statement":[
            {
                "action":"SET",
                "object_id":"#65:33650",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#69:17722",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#66:21901",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#69:21247",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#70:29967",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
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
            "id":"#65:33650",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#69:17722",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#66:21901",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#69:21247",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#70:29967",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        }
    ]
}
```

