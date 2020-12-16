## Добавление статистической записи 'Установка клинической группы' (RcClinicalGroup) указанному пациенту 

### ![POST](../../../../../img/post.png) /patient/record/add
* **Request:** [RcClinicalGroup](../../../../../types/types.md#com.siams.med.api.Rc.RcClinicalGroup) **record** <patient_id, RcClinicalGroup>
* **Response:** [[RcClinicalGroup](../../../../../types/types.md#com.siams.med.api.Rc.RcClinicalGroup)]

Статистическая запись 'Установка клинической группы' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) указанному пациенту.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

```json
{
    "record":{
        "patient_id":"#71:33568",
        "rc_clinical_group":{
            "group_type":{
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
            "id":"#1081:13388",
            "class_name":"RcClinicalGroup",
            "patient_id":"#71:33568",
            "ehr_id":"#1055:33568",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:49:03"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:49:03",
            "rc_clinical_group":{
                "group_type":{
                    "code":"NONE",
                    "caption":""
                }
            }
        }
    ]
}
```
