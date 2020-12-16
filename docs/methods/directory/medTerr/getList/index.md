## Список медицинских территорий

### ![GET](../../../../img/get.png) /medTerr/getList
* **Response:** [[MedTerr](../../../../types/types.md#com.siams.med.api.MedTerr)]

### Пример http
**Request**

GET `https://demo.onco-reg.ru/api/1.0/json/medTerr/getList HTTP/1.1`  
`X-Oncor-API-Token:{{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**
```json
{
  "result": [
    {
      "id": "#33:0",
      "unq": "1.2.643.2.75.1.100.2.66.669999",
      "federal_code": "66",
      "code": "9999",
      "name": "Прочие территории Свердл.обл.",
      "okato": "65000000000"
    },
    {
      "id": "#33:1",
      "unq": "1.2.643.2.75.1.100.2.66.660708",
      "federal_code": "66",
      "code": "708",
      "name": "Малышевский гор. округ",
      "okato": "65409562000"
    },
    {
      "id": "#33:2",
      "unq": "1.2.643.2.75.1.100.2.66.661201",
      "federal_code": "66",
      "code": "1201",
      "name": "Невьянский гор. округ",
      "okato": "65227000000"
    }
  ]
}
```