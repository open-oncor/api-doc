## Добавление направления в указанное заболевание (RcReferral)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcReferral](../../../../../types/types.md#com.siams.med.api.Rc.RcReferral) **record** <patient_id, ehr_id, RcReferral>
* **Response:** [[RcReferral](../../../../../types/types.md#com.siams.med.api.Rc.RcReferral)]

Направление добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

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
        "rc_referral":{
            "purpose":"Цель направления",
            "routing_list":{
                "apply_last_on_any_other_disease_date":"2018-02-01",
                "apply_last_date":"2018-02-01",
                "apply_first_date":"2018-02-01",
                "request_date":"2018-02-01",
                "admission_date":"2018-02-01",
                "examination_lsat_date":"2018-02-01",
                "treatment_first_date":"2018-02-01",
                "expert_opinion":"Экспертное заключение",
                "expert_opinion_date":"2018-02-01",
                "note":"Примечание к направлению",
                "diagnostics":[
                    {
                        "type":{
                            "code":"OAM"
                        },
                        "date":"2018-01-01",
                        "note":"Примечание к обследованию"
                    }
                ]
            }
        }
    }
}
```

**Response**
```json
{
  "result": [
    {
      "id": "#1510:13819",
      "class_name": "RcReferralRL",
      "patient_id": "#65:3583",
      "ehr_id": "#877:4012",
      "published": {
        "user_id": "#961:97",
        "time": "2020-12-15 17:04:56"
      },
      "org_unit_id": "#999:28",
      "time_rc": "2020-12-15 17:04:56",
      "rc_referral": {
        "referral_type": "RF_CONSULT",
        "purpose": "Цель направления",
        "routing_list": {
          "apply_last_on_any_other_disease_date": "2018-02-01",
          "apply_last_date": "2018-02-01",
          "apply_first_date": "2018-02-01",
          "request_date": "2018-02-01",
          "admission_date": "2018-02-01",
          "examination_lsat_date": "2018-02-01",
          "treatment_first_date": "2018-02-01",
          "expert_opinion": "Экспертное заключение",
          "expert_opinion_date": "2018-02-01",
          "note": "Примечание к направлению",
          "referral_code": "1100161",
          "diagnosis": {
            "mkb_code": "C50.1",
            "mkb_name": "Центральной части молочной железы",
            "tnm": {
              "t": {
                "id": "5",
                "code": "T_1",
                "caption": "1"
              },
              "n": {
                "id": "2",
                "code": "N_0",
                "caption": "0"
              },
              "m": {
                "id": "2",
                "code": "M_0",
                "caption": "0"
              },
              "g": {
                "code": "NONE",
                "caption": ""
              }
            },
            "dz_stage": {
              "id": "4",
              "code": "I",
              "caption": "I"
            },
            "how_discover": {
              "orid": "#291:0",
              "id": "1",
              "caption": "обратился сам"
            },
            "morph_class": {
              "orid": "#851:32",
              "code": "8510/3",
              "caption": "8510/3. Медуллярный рак, БДУ"
            },
            "tumor_main": {
              "orid": "#340:0",
              "id": "1",
              "caption": "основная"
            },
            "tumor_side": {
              "orid": "#347:0",
              "id": "1",
              "caption": "слева"
            },
            "plural": {
              "orid": "#307:0",
              "id": "1",
              "caption": "нет"
            }
          },
          "diagnostics": [
            {
              "type": {
                "code": "OAM",
                "caption": "ОАМ"
              },
              "date": "2018-01-01",
              "note": "Примечание к обследованию"
            }
          ]
        }
      }
    }
  ]
}
```
