## Добавление статистической записи 'Постановка на учёт' (RcRegIn) указанному пациенту 

### ![POST](../../../../../img/post.png) /patient/record/add
* **Request:** [RcRegIn](../../../../../types/types.md#com.siams.med.api.Rc.RcRegIn) **record** <patient_id, RcRegIn>
* **Response:** [[RcRegIn](../../../../../types/types.md#com.siams.med.api.Rc.RcRegIn)]

Статистическая запись 'Постановка на учёт' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) указанному пациенту.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

```json
{
    "record":{
        "patient_id":"#70:33669",
        "rc_reg_in":{
            "clause":{
                "code":"NONE"
            }
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1059:46079",
            "class_name":"RcRegIn",
            "patient_id":"#70:33669",
            "ehr_id":"#1054:33669",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:27:52"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:27:52",
            "rc_reg_in":{
                "clause":{
                    "code":"NONE",
                    "caption":"неизвестно"
                }
            }
        }
    ]
}
```
