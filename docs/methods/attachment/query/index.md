## Получение списка вложений по набору их ключей

### ![POST](../../../img/post.png) /attachment/query 
* **Request:** [Query](../../../types/types.md#attachmentquery) 
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Возвращает список вложений В запросе передаётся массив [id](../../../types/types.md#attachmentmeta).

В ответе передаётся массив [Attachment](../../../types/types.md#com.siams.med.api.Attachment) c указанными [id](../../../types/types.md#attachmentmeta).

### Пример http
**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/attachment/query HTTP/1.1`
```json
{
    "query":{
        "ids":[
            "#1585:422"
        ]
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1585:422",
            "digest":"6e4a3290ff2ab22fed4e747c95678bbf534b41d0",
            "name":"проверка.txt",
            "type":"text/plain",
            "size":27,
            "created":"2018-10-02 18:53:06"
        }
    ]
}
```
