## Поиск поиск заявок на ДЭЗО

### ![POST](../../../../img/post.png) /search/start/RcTm66OrderQuery
* **Request:** [RcTm66OrderQuery](../../../../types/types.md#com.siams.med.api.RcTm66OrderQuery) 
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcDocQuery HTTP/1.1`
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
    "result":[
        {
            "id":"23c89dab-2ddb-4bdf-a0c3-d5a33b44ff0e"
        }
    ]
}
```

### Пример java

```java
class SearchRcDoc {
    public static void main(String[] args) throws IOException, InterruptedException {
        final ProtoBuffClient client = newProtoBuffClient();

        final Search.SearchJob job = client.startSearchRcDoc(Search.RcTm66OrderQuery.newBuilder()
                .setFromDate("2018-01-01")
                .setStatusIsNull(true)
                .build());

        SearchUtils.waitForJob(client, job);
    }
}

```

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

