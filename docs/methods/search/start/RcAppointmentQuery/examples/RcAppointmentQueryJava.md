[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcAppointmentQuery](../index.md)

### Java пример

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

**[HTTP примеры](RcAppointmentQuery.md)**