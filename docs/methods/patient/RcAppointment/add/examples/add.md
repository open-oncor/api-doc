[Работа с пациентами](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/patient/RcAppointment/add](../index.md)

### HTTP примеры

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/RcAppointment/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#70:33669",
        "rc_appointment":{
            "rc_referral_id":"#1505:3512",
            "confirmed":false,
            "note":"Example"
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1089:3142",
            "class_name":"RcAppointment",
            "patient_id":"#70:33669",
            "ehr_id":"#876:36710",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-09 00:54:18"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-09 00:54:18",
            "rc_appointment":{
                "rc_referral_id":"#1505:3512",
                "confirmed":false,
                "note":"Example"
            }
        }
    ]
}
```

**[Java пример](addRcAppointmentJava.md)**