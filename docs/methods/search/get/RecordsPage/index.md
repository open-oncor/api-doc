## Постраниченое получение найденных ранее в поисковом запросе записей


### ![POST](../../../../img/post.png) /search/get/RecordsPage
* **Request:** [Page](../../../../types/types.md#com.siams.med.api.Page) 
* **Response:** [[RecordsPage](../../../../types/types.md#com.siams.med.api.RecordsPage)]

Постранично ищет записи. 

В запрос передаётся: 

[Page](../../../../types/types.md#com.siams.med.api.Page)
* required [job](../../../../types/types.md#com.siams.med.api.SearchJob)

В ответ передаётся:
 * [RecordsPage](../../../../types/types.md#com.siams.med.api.RecordsPage)

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/get/RecordsPage HTTP/1.1`
```json
{
    "page":{
        "job":{
            "id":"43153f0a-9865-4943-a856-c30449d4eb0e"
        },
        "offset":0,
        "size":5
    }
}
```

**Response**

```json
{
    "result":[
        {
            "page":{
                "job":{
                    "id":"43153f0a-9865-4943-a856-c30449d4eb0e"
                },
                "offset":0,
                "size":5
            }
        }
    ]
}
```

### Пример java

```java
public class GetRecordsPage {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        final Search.SearchJob job = client.startSearchRcReferral(Search.RcReferralQuery.newBuilder()
                .setFromDate("2016-10-01")
                .setToDate("2019-12-10")
                .setHasAppointment(false)
                .build());

        final Search.RecordsPage recordsPage = client.getSearchRecordsPage(Search.Page.newBuilder()
                .setJob(job)
                .setOffset(0)
                .setSize(5)
                .build());

        Search.Page page = recordsPage.getPage();
    }
}
```