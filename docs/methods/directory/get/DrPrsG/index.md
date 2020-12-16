## Справочник половой принадлежности

### ![GET](../../../../img/get.png) /directory/get/Gender

* **Response: [[DrPrsG](../../../../types/types.md#com.siams.med.api.DrPrsG)]**

В ответе передаётся массив записей из справочника [DrPrsG](../../../../types/types.md#com.siams.med.api.DrPrsG).

### Пример http
**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/DrPrsG HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`    
`Content-Type: application/json`  

**Response**

```json
{
    "result":[
        {
            "orid":"#721:0",
            "id":"1",
            "caption":"М"
        },
        {
            "orid":"#722:0",
            "id":"",
            "caption":"Пол"
        },
        {
            "orid":"#723:0",
            "id":"2",
            "caption":"Ж"
        },
        {
            "orid":"#724:0",
            "id":"3",
            "caption":"не определено"
        }
    ]
}
```
