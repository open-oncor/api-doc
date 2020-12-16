## Добавление пациента

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types/types.md#com.siams.med.api.Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response :** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#com.siams.med.api.ErrorResult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/patient/add HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

```json
{
    "patient":{
        "first_name":"Иван",
        "middle_name":"Иванович",
        "last_name":"Иванов",
        "birth_day":"1901-01-01",
        "gender":{
            "id":"1"
        },
        "phones":"+7 911",
        "address": {
          "address": "г. Верхняя Пышма, ул. Серова, д.34, кв. 56",
          "med_terr": {
            "id": "#35:4",
            "name": "Гор. округ Верхняя Пышма"
          }
        }

    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#65:33650",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "last_name":"Иванов",
            "birth_day":"1901-01-01",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ010101М",
            "ehr_count":0,
            "company_name":"",
            "snils":"",
            "phones":"+7 911",
            "address": {
              "address": "г. Верхняя Пышма, ул. Серова, д.34, кв. 56",
              "med_terr": {
                  "id": "#35:4",
                  "unq": "1.2.643.2.75.1.100.2.66.661102",
                  "federal_code": "66",
                  "code": "1102",
                  "name": "Гор. округ Верхняя Пышма",
                  "okato": "65420000000"
              }
            }

        }
    ]
}
```

**Response `422`**

```json
{
  "error": {
    "name": "com.siams.med.api.PatientAlreadyExistsException",
    "message": "Пациент уже существует",
    "uuid": "f948e19e-3803-4380-819d-61ec0deb0729"
  }
}
```
