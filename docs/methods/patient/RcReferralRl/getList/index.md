## Получение списка направлений пациента


### ![GET](../../../../img/get.png) /patient/RcReferralRL/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../../types/types.md#com.siams.med.api.Rc)]

Возвращает список направлений для пациента с идентификатором [patient_id](../../../../types/types.md#com.siams.med.api.Rc).

В ответе передаётся массив объектов [Rc](../../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request:** GET `https://demo.onco-reg.ru/api/1.0/json/patient/RcReferralRL/getList?patient_id=70:33669 HTTP/1.1`

**Response**
```json
{
  "result": [
    {
      "id": "#1506:0",
      "class_name": "RcReferralRL",
      "patient_id": "#66:6375",
      "ehr_id": "#879:6697",
      "published": {
        "user_id": "#962:0",
        "time": "2018-12-18 10:47:45"
      },
      "org_unit_id": "#993:0",
      "time_rc": "2018-12-18 10:47:44",
      "rc_referral": {
        "referral_type": "RF_CONSULT",
        "purpose": "Цель направления",
        "routing_list": {
          "apply_last_on_any_other_disease_date": "2018-02-01 00:00:00",
          "apply_last_date": "2018-02-01 00:00:00",
          "apply_first_date": "2018-02-01 00:00:00",
          "request_date": "2018-02-01 00:00:00",
          "admission_date": "2018-02-01 00:00:00",
          "examination_lsat_date": "2018-02-01 00:00:00",
          "treatment_first_date": "2018-02-01 00:00:00",
          "health_record_code": "",
          "expert_opinion": "Экспертное заключение",
          "expert_opinion_date": "2018-02-01 00:00:00",
          "note": "Примечание к направлению",
          "referral_code": "1000002",
          "diagnosis": {
            "mkb_code": "C50.4",
            "mkb_name": "Верхненаружного квадранта молочной железы",
            "tnm": {
              "t": {
                "id": "6",
                "code": "T_1A",
                "caption": "1a"
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
              "orid": "#855:30",
              "code": "8500/3",
              "caption": "8500/3. Инфильтрирующий протоковый рак"
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
              "date": "2018-01-01 00:00:00",
              "note": "Примечание к обследованию"
            }
          ]
        }
      }
    },
    {
      "id": "#1507:0",
      "class_name": "RcReferralRL",
      "patient_id": "#66:6375",
      "ehr_id": "#879:6697",
      "published": {
        "user_id": "#962:0",
        "time": "2018-12-18 14:18:31"
      },
      "org_unit_id": "#993:0",
      "time_rc": "2018-12-18 14:18:31",
      "rc_referral": {
        "referral_type": "RF_CONSULT",
        "purpose": "Цель направления",
        "routing_list": {
          "apply_last_on_any_other_disease_date": "2018-02-01 00:00:00",
          "apply_last_date": "2018-02-01 00:00:00",
          "apply_first_date": "2018-02-01 00:00:00",
          "request_date": "2018-02-01 00:00:00",
          "admission_date": "2018-02-01 00:00:00",
          "examination_lsat_date": "2018-02-01 00:00:00",
          "treatment_first_date": "2018-02-01 00:00:00",
          "health_record_code": "",
          "expert_opinion": "Экспертное заключение",
          "expert_opinion_date": "2018-02-01 00:00:00",
          "note": "Примечание к направлению",
          "referral_code": "1000003",
          "diagnosis": {
            "mkb_code": "C50.4",
            "mkb_name": "Верхненаружного квадранта молочной железы",
            "tnm": {
              "t": {
                "id": "6",
                "code": "T_1A",
                "caption": "1a"
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
              "orid": "#855:30",
              "code": "8500/3",
              "caption": "8500/3. Инфильтрирующий протоковый рак"
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
              "date": "2018-01-01 00:00:00",
              "note": "Примечание к обследованию"
            }
          ]
        }
      }
    }
  ]
}
```
