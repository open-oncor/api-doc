[Работа с заболеваниями пациента](../../../../index.md)
=================================

### ![POST](../../../../../../img/post.png) [/ehr/record/add](../../index.md)

### Пример добавления записи [RcOper](../../../../../../types/types.md#rcrcoper)

**Request**

POST `http://tempurl.com/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#65:33650",
        "ehr_id":"#879:35649",
        "rc_oper":{
            "operation":{
                "id":"845"
            },
            "condition":{
                "id":"1"
            },
            "org_unit_id":"#993:1",
            "intra_compl":{
                "orid":"#665:4",
                "id":"37",
                "caption":"01.36. Травма паренхимы печени"
            },
            "after_compl":{
                "orid":"#665:4",
                "id":"37",
                "caption":"01.36. Травма паренхимы печени"
            },
            "srv":[
                {
                    "code":"SRV_1_1_5",
                    "caption":"Регионарных лимфатических узлов без первичной опухоли",
                    "group":1,
                    "index":5
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
            "id":"#1265:14654",
            "class_name":"RcOper",
            "patient_id":"#65:33650",
            "ehr_id":"#879:35649",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:58:34"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:58:34",
            "rc_oper":{
                "operation":{
                    "orid":"#678:115",
                    "id":"845",
                    "caption":"Д06. ДРУГИЕ МЕТОДЫ"
                },
                "condition":{
                    "id":"1",
                    "code":"AMB",
                    "caption":"амбулаторно"
                },
                "org_unit_id":"#993:1",
                "intra_compl":{
                    "orid":"#665:4",
                    "id":"37",
                    "caption":"01.36. Травма паренхимы печени"
                },
                "after_compl":{
                    "orid":"#665:4",
                    "id":"37",
                    "caption":"01.36. Травма паренхимы печени"
                },
                "srv":[
                    {
                        "code":"SRV_1_1_5",
                        "caption":"Регионарных лимфатических узлов без первичной опухоли",
                        "group":1,
                        "index":5
                    }
                ]
            }
        }
    ]
}
```
