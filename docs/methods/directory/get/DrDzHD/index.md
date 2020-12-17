## Справочник обстоятельств выявления заболевания

### ![GET](../../../../img/get.png) /directory/get/DrDzHD
* **Response: [[DrDzHD](../../../../types/types.md#com.siams.med.api.DrDzHD)]**

В ответе передаётся массив записей из справочника [DrDzHD](../../../../types/types.md#com.siams.med.api.DrDzHD).

### Пример http
**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/DrDzHD HTTP/1.1`  
`X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**

```json
{
    "result": [
        {
            "orid": "#289:0",
            "id": "0",
            "caption": "неизвестно"
        },
        {
            "orid": "#290:0",
            "id": "",
            "caption": "Обстоятельства выявления"
        },
        {
            "orid": "#291:0",
            "id": "1",
            "caption": "обратился сам"
        },
        {
            "orid": "#292:0",
            "id": "2",
            "caption": "активно при профосмотре"
        },
        {
            "orid": "#293:0",
            "id": "3",
            "caption": "активно в смотровом кабинете"
        },
        {
            "orid": "#294:0",
            "id": "4",
            "caption": "при других обстоятельствах"
        },
        {
            "orid": "#295:0",
            "id": "5",
            "caption": "посмертно при аутопсии"
        },
        {
            "orid": "#296:0",
            "id": "6",
            "caption": "посмертно без аутопсии"
        }
    ]
}
```
