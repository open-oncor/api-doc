# Замена статуса записи на "Обработка началась"

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/rc/updateInstanceStatus`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

``` json
{
   "updateInstanceStatus":{
       "json":"{status: \"Обработка началась\"}",
       "rc_id":"{{rcId}}"
   }
}
```
**Response**

```json
{
  "result": [
    {
      "json": "{\"status\":\"Обработка началась\"}",
      "rc_id": "#1945:66",
      "user_id": "#961:97",
      "time": "2020-12-17 10:15:26"
    }
  ]
}
```