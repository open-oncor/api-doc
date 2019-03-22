##Поиск предварительных записей на приём для пациента по набору условий

### ![POST](../../../../img/post.png) /search/start/RcAppointmentQuery
* **Request:** [RcAppointmentQuery](../../../../types/types.md#com.siams.med.api.RcAppointmentQuery) **query**
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcAppointmentQuery](../../../../types/types.md#com.siams.med.api.RcAppointmentQuery). 

В ответе передаётся [SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/start/RcAppointmentQuery HTTP/1.1`
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

### Пример java

```java
class SearchRcAppointment {
    public static void main(String[] args) throws IOException, InterruptedException {
        final ProtoBuffClient client = newProtoBuffClient();

        final Search.SearchJob job = client.startSearchRcAppointment(Search.RcAppointmentQuery.newBuilder()
                .setFromDate("2017-10-01")
                .setToDate("2017-12-10")
                .build());

        SearchUtils.waitForJob(client, job);
    }
}

```