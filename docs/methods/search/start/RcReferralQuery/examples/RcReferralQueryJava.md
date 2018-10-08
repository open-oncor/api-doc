[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/start/RcReferralQuery](../index.md)

### Java пример

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

**[HTTP примеры](RcReferralQuery.md)**