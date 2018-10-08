[Работа с вложениями](../../index.md)
=====================================================

### ![POST](../../../../img/get.png) [/attachment/create](../index.md)

### Java пример

```java
public class CreateAttachment {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        final ByteString textData = ByteString.copyFromUtf8("Текстовый файл");
        final Attachments.Attachment.Meta attachment =
                client.createAttachment(Attachments.Attachment
                        .newBuilder()
                        .setData(textData)
                        .setMeta(Attachments.Attachment.Meta
                                .newBuilder()
                                .setName("проверка.txt")
                                .setType("text/plain")
                        )
                        .build());

    }
}
```

**[HTTP примеры](create.md)**