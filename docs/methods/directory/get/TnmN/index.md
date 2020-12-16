## Справочник N

### ![GET](../../../../img/get.png) /directory/get/TnmN
* **Response: [[TnmN](../../../../types/types.md#com.siams.med.api.TnmT)]**

В ответе передаётся массив записей из справочника [TnmN](../../../../types/types.md#com.siams.med.api.TnmN).

### Пример http

**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/TnmN HTTP/1.1`  
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
      "code": "N_X",
      "caption": "X"
    },
    {
      "id": "2",
      "code": "N_0",
      "caption": "0"
    },
    {
      "id": "3",
      "code": "N_1",
      "caption": "1"
    },
    {
      "id": "4",
      "code": "N_1A",
      "caption": "1a"
    },
    {
      "id": "5",
      "code": "N_1B",
      "caption": "1b"
    },
    {
      "id": "6",
      "code": "N_1C",
      "caption": "1c"
    },
    {
      "id": "7",
      "code": "N_2",
      "caption": "2"
    },
    {
      "id": "8",
      "code": "N_2A",
      "caption": "2a"
    },
    {
      "id": "9",
      "code": "N_2B",
      "caption": "2b"
    },
    {
      "id": "10",
      "code": "N_2C",
      "caption": "2c"
    },
    {
      "id": "11",
      "code": "N_3",
      "caption": "3"
    },
    {
      "id": "12",
      "code": "N_3A",
      "caption": "3a"
    },
    {
      "id": "13",
      "code": "N_3B",
      "caption": "3b"
    },
    {
      "id": "14",
      "code": "N_3C",
      "caption": "3c"
    }
  ]
}
```

