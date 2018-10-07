[Работа с вложениями](../index.md)
==================================

### ![POST](../../../../img/post.png) [/attachment/query](../index.md)

```java
public class QueryAttachment {
    public static void main(String[] args) throws IOException {
            newProtoBuffClient().queryAttachment(
                    Attachments.Attachment.Query
                            .newBuilder()
                            .addIds("1586:412")
                            .build()
            );
    }
}
```

**[HTTP примеры](query.md)**