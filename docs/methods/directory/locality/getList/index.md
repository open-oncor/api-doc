## Список населённых пунктов региона

### ![GET](../../../../img/get.png) /locality/getList
* **Response:** [[Locality](../../../../types/types.md#com.siams.med.api.Locality)]



### Пример http

**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/locality/getList HTTP/1.1`  
`X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**
```json
{
  "result": [
    {
      "id": "#1721:0",
      "name": "Екатеринбург",
      "type": "г."
    },
    {
      "id": "#1721:1",
      "name": "Качканар",
      "type": "г."
    },
    {
      "id": "#1721:2",
      "name": "Ревда",
      "type": "г."
    },
    
    {
      "id": "#1649:2",
      "name": "Фурманово",
      "type": "село"
    },
    ...
  ]
}
```
