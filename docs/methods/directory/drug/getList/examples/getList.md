[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/drug/getList](../index.md)

### HTTP примеры

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/drug/getList HTTP/1.1`

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
    }
  ]
}
```
