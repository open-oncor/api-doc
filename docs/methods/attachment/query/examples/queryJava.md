[Работа с вложениями](../index.md)
==================================

### ![POST](../../../../img/post.png) [/attachment/query](../index.md)

### Java пример

```java
public class AttachmentQuery {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Attachments.Attachment.Meta> metaList = client.queryAttachment(
                Attachments.Attachment.Query.newBuilder().addIds("1586:412").build()
        );
    }
}

```

**[HTTP примеры](query.md)**