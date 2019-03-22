## Поиск медицинских документов пациента

### ![POST](../../../../img/post.png) /search/start/RcDocQuery
* **Request:** [RcDocQuery](../../../../types/types.md#com.siams.med.api.RcDocQuery) **query**
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcDocQuery](../../../../types/types.md#com.siams.med.api.RcDocQuery).

В ответе передаётся [SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob).

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcDocQuery HTTP/1.1`
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

        final Search.SearchJob job = client.startSearchRcDoc(Search.RcDocQuery.newBuilder()
                .setFromDate("2018-01-01")
                .build());

        SearchUtils.waitForJob(client, job);
    }
}

```