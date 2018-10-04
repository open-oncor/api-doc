[Работа с пациентами](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/patient/RcAppointment/add](../index.md)

### Примеры

**Request**

POST `http://tempurl.com/patient/RcAppointment/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#66:30293",
        "rc_appointment":{
            "rc_referral_id":"#1505:561",
            "confirmed":true,
            "note":"Проверка"
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1089:2655",
            "class_name":"RcAppointment",
            "patient_id":"#66:30293",
            "ehr_id":"#873:32688",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 21:52:51"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 21:52:51",
            "rc_appointment":{
                "rc_referral_id":"#1505:561",
                "confirmed":true,
                "note":"Проверка"
            }
        }
    ]
}
```