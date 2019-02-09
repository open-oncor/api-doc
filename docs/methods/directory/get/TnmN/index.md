## Справочник N

### ![GET](../../../../img/get.png) /directory/get/TnmN
* **Response: [[TnmN](../../../../types/types.md#com.siams.med.api.TnmT)]**

В ответе передаётся массив записей из справочника [TnmN](../../../../types/types.md#com.siams.med.api.TnmN).

### Примеры

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/TnmN HTTP/1.1`

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
    }      
  ]
}
```

