## Получение описания вложения

### ![GET](../../../img/get.png) /attachment/get`?id={id}`
* **URL parameter:** [id](../../../types/types.md#attachmentmeta)
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

### Пример http
**Request:** GET `https://demo.onco-reg.ru/api/1.0/json/attachment/get?id=#1587:18428 HTTP/1.1`

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

В json формате сообщений поле `result.data` кодируется **Base64**
 
Например строка `0KLQtdC60YHRgtC+0LLRi9C5INGE0LDQudC7` из этого примера содержит
значение `Текстовый файл` в кодировке `UTF-8` 