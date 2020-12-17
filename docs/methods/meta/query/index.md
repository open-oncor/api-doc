## Получение массива метаданных

### ![POST](../../../img/post.png) /meta/query
* **Request:** [Query](../../../types/types.md#com.siams.med.api.Query) 
* **Response:** [[Meta.proto](../../../types/types.md#metaproto)]

Возвращает список метаданных [Meta.proto](../../../types/types.md#metaproto) 
для объектов с указанными [id](../../../types/types.md#metaproto)



**Пример http**

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/meta/query HTTP/1.1`              
      `X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`   
      `Content-Type: application/json`
      
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


