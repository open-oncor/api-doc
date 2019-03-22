[Работа с поиском](../../index.md)
==================================

### ![POST](../../../../img/post.png) /search/start/RcReferralQuery
* **Request:** [RcReferralQuery](../../../../types/types.md#com.siams.med.api.RcReferralQuery) **query**
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcReferralQuery](../../../../types/types.md#com.siams.med.api.RcReferralQuery).

В ответе передаётся [SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcReferralQuery HTTP/1.1`
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
            "id":"a8a10778-dc14-41cc-ac97-4db300fa99a4"
        }
    ]
}
```

### Пример java

```java
public class Temp {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Search.SearchJob searchJob = client.startSearchRcReferral(Search.RcReferralQuery.newBuilder()
                .setFromDate("2017-10-01")
                .setToDate("2019-12-10")
                .setHasAppointment(false)
                .build());
    }
}
```