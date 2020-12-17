## Добавление статистической записи 'Гормонотерапия' в указанное заболевание (RcHorm)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcHorm](../../../../../types/types.md#com.siams.med.api.Rc.RcHorm) **record** <patient_id, ehr_id, RcHorm>
* **Response:** [[RcHorm](../../../../../types/types.md#com.siams.med.api.Rc.RcHorm)]

Статистическая запись 'Гормонотерапия' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
    "record":{
        "patient_id":"#65:3583",
        "ehr_id":"#877:4012",
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
  "result": [
    {
      "id": "#1185:3797",
      "class_name": "RcHorm",
      "patient_id": "#65:3583",
      "ehr_id": "#877:4012",
      "published": {
        "user_id": "#961:97",
        "time": "2020-12-16 09:01:54"
      },
      "org_unit_id": "#999:28",
      "time_rc": "2020-12-16 09:01:54",
      "rc_horm": {
        "time_rc_in": "2018-10-04",
        "time_rc_out": "2018-10-04",
        "kind": {
          "xrt": true
        },
        "aim": {
          "code": "NONE",
          "caption": "неизвестно"
        },
        "condition": {
          "code": "NONE",
          "caption": ""
        },
        "compl": {
          "orid": "#667:0",
          "id": "1",
          "caption": "01. ИНТРАОПЕРАЦИОННЫЕ ОСЛОЖНЕНИЯ"
        },
        "drugs": [
          {
            "drug": {
              "orid": "#1545:57",
              "name": "Преднизолон",
              "type": {
                "id": "2",
                "code": "HT",
                "caption": "гормонотерапия"
              },
              "code": "Ю001"
            },
            "dose": 123.0,
            "unit": {
              "id": "3",
              "code": "MKG",
              "caption": "мкг"
            }
          }
        ]
      }
    }
  ]
}
```
