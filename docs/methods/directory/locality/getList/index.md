## Список населённых пунктов региона

### ![GET](../../../../img/get.png) /locality/getList
* **Response:** [[Locality](../../../../types/types.md#com.siams.med.api.Locality)]



### Пример http

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/locality/getList HTTP/1.1`

**Response**
```json
{
  "result": [
    {
      "id": "#1649:0",
      "name": "Владивосток",
      "type": "город"
    },
    {
      "id": "#1649:1",
      "name": "Партизанск",
      "type": "город"
    },
    {
      "id": "#1649:2",
      "name": "Фурманово",
      "type": "село"
    }
  ]
}
```

### Пример java
