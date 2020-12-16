## Справочник T

### ![GET](../../../../img/get.png) /directory/get/TnmT
* **Response: [[TnmT](../../../../types/types.md#com.siams.med.api.TnmT)]**

В ответе передаётся массив записей из справочника [TnmT](../../../../types/types.md#com.siams.med.api.TnmT).

### Пример http

**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/TnmT HTTP/1.1
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}
Content-Type: application/json`

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
      "code": "T_X",
      "caption": "X"
    },
    {
      "id": "2",
      "code": "T_0",
      "caption": "0"
    },
    {
      "id": "3",
      "code": "T_IS",
      "caption": "is"
    },
    {
      "id": "4",
      "code": "T_A",
      "caption": "a"
    },
    {
      "id": "5",
      "code": "T_1",
      "caption": "1"
    },
    {
      "id": "6",
      "code": "T_1A",
      "caption": "1a"
    },
    {
      "id": "7",
      "code": "T_1A1",
      "caption": "1a1"
    },
    {
      "id": "8",
      "code": "T_1A2",
      "caption": "1a2"
    },
    {
      "id": "9",
      "code": "T_1B",
      "caption": "1b"
    },
    {
      "id": "10",
      "code": "T_1C",
      "caption": "1c"
    },
    {
      "id": "11",
      "code": "T_2",
      "caption": "2"
    },
    {
      "id": "12",
      "code": "T_2A",
      "caption": "2a"
    },
    {
      "id": "13",
      "code": "T_2B",
      "caption": "2b"
    },
    {
      "id": "14",
      "code": "T_2C",
      "caption": "2c"
    },
    {
      "id": "15",
      "code": "T_3",
      "caption": "3"
    },
    {
      "id": "16",
      "code": "T_3A",
      "caption": "3a"
    },
    {
      "id": "17",
      "code": "T_3B",
      "caption": "3b"
    },
    {
      "id": "18",
      "code": "T_3C",
      "caption": "3c"
    },
    {
      "id": "19",
      "code": "T_4",
      "caption": "4"
    },
    {
      "id": "20",
      "code": "T_4A",
      "caption": "4a"
    },
    {
      "id": "21",
      "code": "T_4B",
      "caption": "4b"
    },
    {
      "id": "22",
      "code": "T_4C",
      "caption": "4c"
    },
    {
      "id": "23",
      "code": "T_4D",
      "caption": "4d"
    }
  ]
}
```

