## Справочник M

### ![GET](../../../../img/get.png) /directory/get/TnmM
* **Response: [[TnmM](../../../../types/types.md#com.siams.med.api.TnmM)]**

В ответе передаётся массив записей из справочника [TnmM](../../../../types/types.md#com.siams.med.api.TnmM).

### Пример http

**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/TnmM HTTP/1.1`  
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}  
Content-Type: application/json

**Response**
```json
{
  "result": [
    {
      "code": "NONE",
      "caption": ""
    },
    {
      "id": "1",
      "code": "M_X",
      "caption": "X"
    },
    {
      "id": "2",
      "code": "M_0",
      "caption": "0"
    },
    {
      "id": "3",
      "code": "M_1",
      "caption": "1"
    },
    {
      "id": "4",
      "code": "M_1A",
      "caption": "1a"
    },
    {
      "id": "5",
      "code": "M_1B",
      "caption": "1b"
    }
  ]
}
```

