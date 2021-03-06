## Изменение данных пациента

### ![POST](../../../img/post.png) /patient/update
* **Request:** [PatientUpdate](../../../types/types.md#com.siams.med.api.PatientUpdate) **patient <id, code>**
* **Response:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/patient/update HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`


```json
{
    "patient_update":{
            "id": "#65:33650",
            "code": "ИИИ010101М",
            "entry":[
             { 
               "address": {
                 "med_terr": {
                    "id": "#33:1",
                    "name": "Малышевский гор. округ"
                 },
                 "locality": {
                    "id": "#1721:0",
                    "name": "Екатеринбург",
                    "type": "г."
                 },
                 "living_area_type": {
                    "code": "1",
                    "caption": "Город"
                 }
               }
             }
            ] 
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"#70:33669",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "last_name":"Иванов",
            "birth_day":"1954-01-01",
            "code":"ИИИ010154",
            "ehr_count":1,
            "company_name":"",
            "snils":"Пример снилса",
            "address": {
                            "med_terr": {
                                "id": "#33:1",
                                "unq": "1.2.643.2.75.1.100.2.66.660708",
                                "federal_code": "66",
                                "code": "708",
                                "name": "Малышевский гор. округ",
                                "okato": "65409562000"
                            },
                            "locality": {
                                "id": "#1721:0",
                                "name": "Екатеринбург",
                                "type": "г."
                            },
                            "living_area_type": {
                                "orid": "#41:0",
                                "code": "1",
                                "caption": "Город"
                            }
            }
        }
    ]
}
```
