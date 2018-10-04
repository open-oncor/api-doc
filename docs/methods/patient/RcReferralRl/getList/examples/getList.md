[Работа с пациентами](../../../index.md)
=====================================

### ![GET](../../../../../img/get.png) [/patient/RcReferralRL/getList`?patient_id={patient_id}`](../index.md)

### Примеры

**Request:** GET `http://tempurl.com/patient/RcReferralRL/getList?patient_id=71:30320 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "id":"#1505:730",
            "class_name":"RcReferralRL",
            "patient_id":"#71:30320",
            "ehr_id":"#879:32656",
            "published":{
                "user_id":"#963:30",
                "time":"2017-12-06 15:26:05"
            },
            "org_unit_id":"#996:21",
            "time_rc":"2017-12-06 15:21:57",
            "rc_referral":{
                "rc_appointment_id":"#1089:656",
                "referral_org_unit_id":"#999:28",
                "referral_type":"RF_CONSULT",
                "routing_list":{
                    "note":"Киста левого яичника.",
                    "referral_code":"1003899",
                    "diagnosis":{
                        "mkb_code":"D27",
                        "mkb_name":"Доброкачественное новообразование яичника",
                        "tnm":{
                            "t":{
                                "code":"NONE",
                                "caption":""
                            },
                            "n":{
                                "code":"NONE",
                                "caption":""
                            },
                            "m":{
                                "code":"NONE",
                                "caption":""
                            },
                            "g":{
                                "code":"NONE",
                                "caption":""
                            }
                        },
                        "dz_stage":{
                            "code":"NONE",
                            "caption":""
                        }
                    },
                    "diagnostics":[
                        {
                            "type":{
                                "id":"US_PELVIC",
                                "caption":"УЗИ малого таза"
                            },
                            "date":"2016-10-27 00:00:00"
                        }
                    ]
                }
            }
        }
    ]
}
```