## Список препаратов

### ![GET](../../../../img/get.png) /drug/getList
* **Response:** [[DrugRecord](../../../../types/types.md#com.siams.med.api.DrugRecord)]


### Пример http
**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/drug/getList HTTP/1.1`  
    `X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
    `Content-Type: application/json`

**Response**
```json
{
  "result": [
    {
      "orid": "#1545:0",
      "name": "Азотоиперит (Azotoyperit - эмбихин)",
      "type": {
        "code": "NONE",
        "caption": ""
      },
      "code": "А1.001"
    },
    {
      "orid": "#1545:1",
      "name": "Допан (Dopanum)",
      "type": {
        "code": "NONE",
        "caption": ""
      },
      "code": "А1.009"
    },
    {
      "orid": "#1545:2",
      "name": "Клафен (Clafen - циклофосфан)",
      "type": {
        "code": "NONE",
        "caption": ""
      },
      "code": "А1.017"
    },
    ...
  ]
}
```