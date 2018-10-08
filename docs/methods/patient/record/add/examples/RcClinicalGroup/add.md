[Работа с пациентами](../../../../index.md)
=====================================

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

### HTTP примеры

**Request**

POST http://dev.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1

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

**[Java пример](addJava.md)**