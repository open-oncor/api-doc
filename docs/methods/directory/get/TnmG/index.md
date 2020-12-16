## Справочник G

### ![GET](../../../../img/get.png) /directory/get/TnmG
* **Response: [[TnmG](../../../../types/types.md#com.siams.med.api.TnmG)]**

В ответе передаётся массив записей из справочника [TnmG](../../../../types/types.md#com.siams.med.api.TnmG).

## Пример http

**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/TnmG HTTP/1.1`  
`X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
`Content-Type: application/json` 

**Response**
```json
{
  "result": [
    {
      "code": "NONE",
      "caption": ""
    },
    {
      "code": "G_X",
      "caption": "X"
    },
    {
      "code": "G_1",
      "caption": "1"
    },
    {
      "code": "G_2",
      "caption": "2"
    },
    {
      "code": "G_3",
      "caption": "3"
    },
    {
      "code": "G_4",
      "caption": "4"
    }
  ]
}
```

