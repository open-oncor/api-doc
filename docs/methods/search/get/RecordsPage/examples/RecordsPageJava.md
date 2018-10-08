[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/get/RecordsPage](../index.md)

### Java пример

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

**[HTTP пример](RecordsPage.md)**