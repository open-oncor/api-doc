## Справочник G

### ![GET](../../../../img/get.png) /directory/get/TnmG
* **Response: [[TnmG](../../../../types/types.md#com.siams.med.api.TnmG)]**

В ответе передаётся массив записей из справочника [TnmG](../../../../types/types.md#com.siams.med.api.TnmG).

## Пример (http)

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/TnmG HTTP/1.1`

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
      "code": "G_X",
      "caption": "X"
    }  
  ]
}
```

