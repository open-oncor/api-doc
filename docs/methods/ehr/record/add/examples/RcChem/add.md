### Пример добавления записи RcChem (http)

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)


**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#66:33485",
        "ehr_id":"#873:36390",
        "rc_chem":{
            "time_rc_in":"2018-10-04 23:52:33",
            "time_rc_out":"2018-10-04 23:52:33",
            "aim":{
                "code":"NONE"
            },
            "kind":{
                "code":"NONE"
            },
            "condition":{
                "code":"NONE"
            },
            "compl":{
                "id":"1"
            },
            "drugs":[
                {
                    "drug":{
                        "code":"Э001"
                    },
                    "dose":123.0,
                    "unit":{
                        "code":"MKG"
                    }
                }
            ],
            "srv":[
                {
                    "code":"SRV_4_1_1"
                }
            ]
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1122:17250",
            "class_name":"RcChem",
            "patient_id":"#66:33485",
            "ehr_id":"#873:36390",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:52:34"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:52:33",
            "rc_chem":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```

