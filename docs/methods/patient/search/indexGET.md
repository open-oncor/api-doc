## Поиск пациентов
### ![GET](../../../img/get.png) /patient/search`?name=Иванов%20Иван%20Иванович&dob=311288&gender=M&limit=20`
* **URL parameter: name=last_name%20first_name%20middle_name&dob(date of birth)=031267&gender=M&limit=20**
* **Response:** [[PatientSearchResult](../../../types/types.md#com.siams.med.api.PatientSearchResult)]


Возвращает массив пациентов в соответствии с запросом или пустой массив, если не найдено ни одного пациента. 

### Пример http

**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/patient/search?name=Иванов%20Иван%20Иванович&dob=031267&gender=M&limit=20 HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response `200`**

```json
{
    "result":[
        {
            "id":"#70:33669",
            "last_name":"Иванов",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "birth_day":"1967-12-03",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ031267М",
            "ehr_count":1,
            "company_name":"",
            "snils":"",
            "address":{
                "address":"",
                "federal_code":"",
                "region_code":"",
                "town":" Каменск-Уральский",
                "street":"",
                "house":"",
                "flat":"",
                "postal_code":"",
                "fias":"",
                "kladr":"",
                "okato":"",
                "med_terr_unq":"1.2.643.2.75.1.100.2.66.660800",
                "living_area_type":{
                    "id":"1"
                }
            }
        }
    ]
}
```
