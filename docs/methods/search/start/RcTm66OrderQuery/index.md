## Поиск заявок на ДЭЗО без статуса

### ![POST](../../../../img/post.png) /search/start/RcTm66OrderQuery
* **Request:** [RcTm66OrderQuery](../../../../types/types.md#com.siams.med.api.RcTm66OrderQuery) 
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

### Структура сообщений ProtoBuffer

```proto
message SearchJob {
    required string id = 1;
    oneof status {
        bool ready = 2;
        ErrorResult error = 3;
    }
}

message RcTm66OrderQuery {
    optional string from_date = 1;
    optional string to_date = 2;
    oneof status {
        bool status_is_null = 3;
        string status_value = 4;
        string status_value_with_history = 5;
    }
}
```

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/search/start/RcTm66OrderQuery HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
    "query":{
        "from_date":"2018-01-01",
        "status_is_null": true
    }
}
```

**Response**

```json
{
  "result": [
    {
      "id": "e3585aea-cf1c-4766-aa4b-afcf93c2d6d5"
    }
  ]
}
```