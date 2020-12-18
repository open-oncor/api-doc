## Поиск направлений по набору условий

### ![POST](../../../../img/post.png) /search/start/RcReferralQuery
* **Request:** [RcReferralQuery](../../../../types/types.md#com.siams.med.api.RcReferralQuery) 
* **Response:** [[SearchJob](../../../../types/types.md#com.siams.med.api.SearchJob)]

### Пример http

**Request**

POST `POST https://demo.onco-reg.ru/api/1.0/json/search/start/RcReferralQuery HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

```json
{
    "query":{
        "has_appointment":false,
        "from_date":"2017-10-01",
        "to_date":"2019-12-10"
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"a8a10778-dc14-41cc-ac97-4db300fa99a4"
        }
    ]
}
```

