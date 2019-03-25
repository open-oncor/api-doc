##Получение описания вложения

### ![GET](../../../img/get.png) /attachment/get`?id={id}`
* **URL parameter:** [id](../../../types/types.md#attachmentmeta)
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Возвращает объект типа [Attachment](../../../types/types.md#com.siams.med.api.Attachment) с идентификатором [id](../../../types/types.md#attachmentmeta)

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

### Пример http
**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/attachment/get?id=1586:412 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "meta":{
                "id":"#1586:412",
                "digest":"6e4a3290ff2ab22fed4e747c95678bbf534b41d0",
                "name":"проверка.txt",
                "type":"text/plain",
                "size":27,
                "created":"2018-10-02 18:53:06"
            },
            "data":"0KLQtdC60YHRgtC+0LLRi9C5INGE0LDQudC7"
        }
    ]
}
```



### Пример java
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