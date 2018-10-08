[Работа с заболеваниями пациента](../../../../index.md)
=================================

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Пример добавления записи [RcRay](../../../../../../types/types.md#rcrcray)

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`

```json
{
    "record":{
        "patient_id":"#68:33232",
        "ehr_id":"#875:36094",
        "rc_ray":{
            "time_rc_in":"2018-10-04 23:59:53",
            "time_rc_out":"2018-10-04 23:59:53",
            "aim":{
                "code":"NONE"
            },
            "kind":{
                "code":"NONE"
            },
            "method":{
                "code":"NONE"
            },
            "way":{
                "code":"NONE"
            },
            "radio":{
                "code":"NONE"
            },
            "doze":1.0,
            "doze_meta":1.0,
            "condition":{
                "code":"NONE"
            },
            "compl":{
                "id":"1"
            },
            "session_count":1,
            "srv":[
                {
                    "code":"SRV_3_1_1"
                }
            ]
        }
    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#1275:8662",
            "class_name":"RcRay",
            "patient_id":"#68:33232",
            "ehr_id":"#875:36094",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:59:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:59:53",
            "rc_ray":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```

**[Java пример](addJava.md)**