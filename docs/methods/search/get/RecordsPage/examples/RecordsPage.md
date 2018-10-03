[Работа с поиском](../../../index.md)
=====================================

### ![POST](../../../../../img/post.png) [/search/get/RecordsPage](../index.md)

### Examples

**URI** `http://tempurl.com/search/get/RecordsPage HTTP/1.1`

**Request**

```json
{
    "page":{
        "job":{
            "id":"cebb037d-9902-405a-995c-5345ca045fc4"
        },
        "offset":0,
        "size":1
    }
}
```

**Response**

```json
{
    "result":[
        {
            "page":{
                "job":{
                    "id":"cebb037d-9902-405a-995c-5345ca045fc4",
                    "ready":true
                },
                "offset":0,
                "size":1
            },
            "rc":[
                {
                    "id":"#1089:244",
                    "class_name":"RcAppointment",
                    "patient_id":"#70:28792",
                    "ehr_id":"#879:30865",
                    "published":{
                        "user_id":"#961:15",
                        "time":"2017-09-01 08:18:03"
                    },
                    "org_unit_id":"#999:28",
                    "time_rc":"2017-09-01 07:48:55",
                    "rc_appointment":{
                        "rc_referral_id":"#1506:225",
                        "confirmed":true,
                        "department":"поликлиника",
                        "doctor":"химиотерапевт",
                        "consulting_room":"313",
                        "consulting_date":"2017-10-04 10:28:00",
                        "note":"за 30 мин. до приема подойти в регистратуру с документами (паспорт, полис, направление, СНИЛС)."
                    }
                }
            ],
            "size":2032
        }
    ]
}
```