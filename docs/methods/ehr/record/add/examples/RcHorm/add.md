[Работа с заболеваниями пациента](../../../../index.md)
=================================

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Пример добавления записи [RcHorm](../../../../../../types/types.md#rcrchorm)

**Request**

POST `http://tempurl.com/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#67:33340",
        "ehr_id":"#874:36231",
        "rc_horm":{
            "time_rc_in":"2018-10-04 23:54:05",
            "time_rc_out":"2018-10-04 23:54:05",
            "kind":{
                "xrt":true
            },
            "aim":{
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
                        "code":"Ю001"
                    },
                    "dose":123.0,
                    "unit":{
                        "code":"MKG"
                    }
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
            "id":"#1185:2310",
            "class_name":"RcHorm",
            "patient_id":"#67:33340",
            "ehr_id":"#874:36231",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:54:05"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:54:05",
            "rc_horm":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```