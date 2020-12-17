## Добавление вложения для заключения



### ![POST](../../../img/post.png) /attachment/create
* **Request:** [Attachment](../../../types/types.md#com.siams.med.api.Attachment) 
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Создаёт новое вложение. 

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)


### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/attachment/create HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

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
> {% // запоминаем id в attachmentId
client.global.set("attachmentId", response.body.result[0].id);
%}
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