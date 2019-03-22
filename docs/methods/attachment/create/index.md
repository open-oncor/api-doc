##Добавление вложения



### ![POST](../../../img/post.png) /attachment/create
* **Request:** [Attachment](../../../types/types.md#com.siams.med.api.Attachment) 
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Создаёт новое вложение. 

В запросе передаётся [Attachment](../../../types/types.md#com.siams.med.api.Attachment). 

В ответе передаётся [Attachment](../../../types/types.md#com.siams.med.api.Attachment).

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)


### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/attachment/create HTTP/1.1`
```json
{
    "attachment":{
        "meta":{
            "name":"проверка.txt",
            "type":"text/plain"
        },
        "data":"0KLQtdC60YHRgtC+0LLRi9C5INGE0LDQudC7"
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1586:412",
            "digest":"6e4a3290ff2ab22fed4e747c95678bbf534b41d0",
            "name":"проверка.txt",
            "type":"text/plain",
            "size":27,
            "created":"2018-10-02 18:53:06"
        }
    ]
}
```

### Пример java

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