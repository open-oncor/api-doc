## Добавление статистической записи 'Лучевая терапия' в указанное заболевание (RcRay)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcRay](../../../../../types/types.md#com.siams.med.api.Rc.RcRay) **record** <patient_id, ehr_id, RcRay>
* **Response:** [[RcRay](../../../../../types/types.md#com.siams.med.api.Rc.RcRay)]

Статистическая запись 'Лучевая терапия' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`

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
  "result": [
    {
      "id": "#1274:11222",
      "class_name": "RcRay",
      "patient_id": "#65:3583",
      "ehr_id": "#877:4012",
      "published": {
        "user_id": "#961:97",
        "time": "2020-12-16 08:40:47"
      },
      "org_unit_id": "#999:28",
      "time_rc": "2020-12-16 08:40:47",
      "rc_ray": {
        "time_rc_in": "2018-10-04",
        "time_rc_out": "2018-10-04",
        "aim": {
          "code": "NONE",
          "caption": "неизвестно"
        },
        "kind": {
          "code": "NONE",
          "caption": "Вид лучевой терапии неизвестен"
        },
        "method": {
          "code": "NONE",
          "caption": "Метод лучевой терапии неизвестен"
        },
        "way": {
          "code": "NONE",
          "caption": "неизвестно"
        },
        "radio": {
          "code": "NONE",
          "caption": "неизвестно"
        },
        "doze": 1.0,
        "doze_meta": 1.0,
        "condition": {
          "code": "NONE",
          "caption": ""
        },
        "compl": {
          "orid": "#667:0",
          "id": "1",
          "caption": "01. ИНТРАОПЕРАЦИОННЫЕ ОСЛОЖНЕНИЯ"
        },
        "session_count": 1
      }
    }
  ]
}
```

