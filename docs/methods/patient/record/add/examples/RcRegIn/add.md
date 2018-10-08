[Работа с пациентами](../../../../index.md)
=====================================

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`
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

**[Java пример](addJava.md)**