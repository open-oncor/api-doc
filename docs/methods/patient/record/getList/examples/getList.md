[Работа с пациентами](../../../index.md)
==================================

### ![GET](../../../../../img/get.png) [/patient/record/getList`?patient_id={patient_id}`](../index.md)

### HTTP примеры

**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/patient/record/getList?patient_id=70:33669 HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"#1060:45958",
            "class_name":"RcRegIn",
            "patient_id":"#70:33669",
            "ehr_id":"#1054:33669",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:27:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:27:53",
            "rc_reg_in":{
                "clause":{
                    "code":"NONE",
                    "caption":"неизвестно"
                }
            }
        },
        {
            "id":"#1068:19100",
            "class_name":"RcRegOut",
            "patient_id":"#70:33669",
            "ehr_id":"#1054:33669",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:27:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:27:53",
            "rc_reg_out":{
                "reason":{
                    "code":"NONE",
                    "caption":""
                }
            }
        }
    ]
}
```

**[Java пример](getListJava.md)**