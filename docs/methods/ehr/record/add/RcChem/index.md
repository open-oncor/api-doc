## Добавление статистической записи 'Химиотерапия' в указанное заболевание (RcChem)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcChem](../../../../../types/types.md#com.siams.med.api.Rc.RcChem) **record** <patient_id, ehr_id, RcChem>
* **Response:** [[RcChem](../../../../../types/types.md#com.siams.med.api.Rc.RcChem)]

Статистическая запись 'Химиотерапия' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

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
  "result": [
    {
      "id": "#1121:30773",
      "class_name": "RcChem",
      "patient_id": "#65:3583",
      "ehr_id": "#877:4012",
      "published": {
        "user_id": "#961:97",
        "time": "2020-12-16 08:56:13"
      },
      "org_unit_id": "#999:28",
      "time_rc": "2020-12-16 08:56:13",
      "rc_chem": {
        "time_rc_in": "2018-10-04",
        "time_rc_out": "2018-10-04",
        "aim": {
          "code": "NONE",
          "caption": "неизвестно"
        },
        "kind": {
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
              "orid": "#1546:57",
              "name": "диферелин",
              "type": {
                "id": "1",
                "code": "CTX",
                "caption": "химиотерапия"
              },
              "code": "Э001"
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
