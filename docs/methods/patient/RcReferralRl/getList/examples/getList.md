[Работа с пациентами](../../../index.md)
=====================================

### ![GET](../../../../../img/get.png) [/patient/RcReferralRL/getList`?patient_id={patient_id}`](../index.md)

### HTTP примеры

**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/patient/RcReferralRL/getList?patient_id=70:33669 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "id":"#1505:3512",
            "class_name":"RcReferralRL",
            "patient_id":"#70:33669",
            "ehr_id":"#876:36710",
            "published":{
                "user_id":"#961:0",
                "time":"2018-10-09 00:49:27"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-09 00:49:23",
            "rc_referral":{
                "rc_appointment_id":"#1089:3142",
                "referral_org_unit_id":"#993:34",
                "referral_type":"RF_CONSULT",
                "routing_list":{
                    "apply_last_date":"2018-10-09 00:49:23",
                    "apply_first_date":"2018-10-09 00:49:23",
                    "referral_code":"1023388",
                    "diagnosis":{
                        "mkb_code":"C00",
                        "mkb_name":"Злокачественные новообразования губы",
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
                    }
                }
            }
        }
    ]
}
```

**[Java пример](getListJava.md)**