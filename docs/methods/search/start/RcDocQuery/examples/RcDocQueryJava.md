[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcDocQuery](../index.md)

### Java пример

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

**[HTTP примеры](RcDocQuery.md)**