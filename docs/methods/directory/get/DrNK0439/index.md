## Справочник осложнений

### ![GET](../../../../img/get.png) /directory/get/DrNK0439
* **Response: [[DrNK0439](../../../../types/types.md#com.siams.med.api.DrNK0439)]**

В ответе передаётся массив записей из справочника [DrNK0439](../../../../types/types.md#com.siams.med.api.DrNK0439).


### Пример http
**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/DrNK0439 HTTP/1.1`  
`X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**

```json
{
    "result":[
        {
            "orid":"#665:0",
            "id":"10",
            "caption":"01.09. Кровотечение паренхиматозное"
        },
        {
            "orid":"#665:1",
            "id":"16",
            "caption":"01.15. Ожоговые поражения при фотодинамической терапии"
        },
        {
            "orid":"#665:2",
            "id":"23",
            "caption":"01.22. Повреждение стенки магистрального сосуда брюшной полости"
        },
        {
            "orid":"#665:3",
            "id":"3",
            "caption":"01.02. Аспирация в противоположное легкое"
        },
        {
            "orid":"#665:4",
            "id":"37",
            "caption":"01.36. Травма паренхимы печени"
        },
        {
            "orid":"#665:5",
            "id":"44",
            "caption":"01.43. Тромбоз артериального анастомоза"
        },
        {
            "orid":"#665:6",
            "id":"111",
            "caption":"06. ОСЛОЖНЕНИЯ ВОСПАЛИТЕЛЬНОГО ХАРАКТЕРА"
        },
        {
            "orid":"#665:7",
            "id":"120",
            "caption":"06.09. Панкреатит"
        },
        ...
    ]
}
```
