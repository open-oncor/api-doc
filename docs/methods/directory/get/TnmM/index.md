### Справочник M

### ![GET](../../../../img/get.png) /directory/get/TnmM
* **Response: [[TnmM](../../../../types/types.md#com.siams.med.api.TnmM)]**

В ответе передаётся массив записей из справочника [TnmM](../../../../types/types.md#com.siams.med.api.TnmM).

#### Примеры

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/TnmM HTTP/1.1`

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
    }  
  ]
}
```

