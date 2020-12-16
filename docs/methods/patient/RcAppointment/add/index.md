## Добавление предварительной записи пациента на приём


### ![POST](../../../../img/post.png) /patient/RcAppointment/add
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) record
* **Response:** [Rc](../../../../types/types.md#com.siams.med.api.Rc)

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/patient/RcAppointment/add HTTP/1.1`
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
