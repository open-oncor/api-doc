## Поиск предварительных записей на приём для пациента по набору условий

### ![POST](../../../../img/post.png) /search/start/RcAppointmentQuery
* **Request:** [RcAppointmentQuery](../../../../types/types.md#com.siams.med.api.RcAppointmentQuery) 
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/search/start/RcAppointmentQuery HTTP/1.1`
```json
{
    "query":{
        "from_date":"2017-10-01",
        "to_date":"2017-12-10"
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"cebb037d-9902-405a-995c-5345ca045fc4"
        }
    ]
}
```

