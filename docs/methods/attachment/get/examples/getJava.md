[Работа с вложениями](../../index.md)
=====================================================

### ![GET](../../../../img/get.png) [/attachment/get`?id={id}`](../index.md)

### Java пример

```java
public class GetAttachment {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();
        Attachments.Attachment attachment = client.getAttachment("1586:412");

        ByteString data = attachment.getData();
        Attachments.Attachment.Meta meta = attachment.getMeta();
    }
}

```

**[HTTP примеры](get.md)**