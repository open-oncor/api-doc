[Работа с вложениями](../../index.md)
=====================================================

### ![GET](../../../../img/get.png) [/attachment/get`?id={id}`](../index.md)

### HTTP примеры

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

**[Пример Java](getJava.md)**