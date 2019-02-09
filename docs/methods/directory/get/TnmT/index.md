### Справочник T

### ![GET](../../../../img/get.png) /directory/get/TnmT
* **Response: [[TnmT](../../../../types/types.md#com.siams.med.api.TnmT)]**

В ответе передаётся массив записей из справочника [TnmT](../../../../types/types.md#com.siams.med.api.TnmT).

#### Примеры

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/TnmT HTTP/1.1`

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
    }  
  ]
}
```

