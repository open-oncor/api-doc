## Получение списка медицинских записей пациента для указанного заболевания

### ![GET](../../../img/get.png) /rc/getList`?ehr_id={ehr_id}`
* **URL parameter:** [ehr_id](../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../types/types.md#com.siams.med.api.Rc)]

Возвращает список записей [Rc](../../../types/types.md#com.siams.med.api.Rc) для указанного заболевания c идентификатором [ehr_id](../../../types/types.md#com.siams.med.api.Rc)

### Пример http

**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/rc/getList?ehr_id=873:43666 HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**
```json
{
  "result": [
    {
      "id": "#884:62309",
      "class_name": "RcDz",
      "patient_id": "#71:40788",
      "ehr_id": "#873:43666",
      "published": {
        "user_id": "#961:335",
        "time": "2019-12-18 10:25:19"
      },
      "org_unit_id": "#999:14",
      "time_rc": "2019-12-02 10:23:07",
      "rc_dz": {
        "diagnosis": {
          "icd10": {
            "orid": "#847:156",
            "code": "C61",
            "caption": "Злокачественное новообразование предстательной железы"
          },
          "status": {
            "orid": "#331:0",
            "id": "9",
            "caption": "окончательный"
          },
          "primacy": {
            "orid": "#315:0",
            "id": "1",
            "caption": "впервые"
          },
          "morph_class": {
            "orid": "#853:10",
            "code": "8140/3",
            "caption": "8140/3. Аденокарцинома, БДУ"
          },
          "tumor_main": {
            "orid": "#340:0",
            "id": "1",
            "caption": "основная"
          },
          "how_discover": {
            "orid": "#291:0",
            "id": "1",
            "caption": "обратился сам"
          },
          "method": {
            "orid": "#299:0",
            "id": "1",
            "caption": "морфологический"
          },
          "plural": {
            "orid": "#307:0",
            "id": "1",
            "caption": "нет"
          },
          "loc_met": {},
          "tnm": {
            "t": {
              "id": "11",
              "code": "T_2",
              "caption": "2"
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
          "stage": {
            "id": "8",
            "code": "II",
            "caption": "II"
          }
        }
      }
    },
    {
      "id": "#893:15011",
      "class_name": "RcSpecTreat",
      "patient_id": "#71:40788",
      "ehr_id": "#873:43666",
      "published": {
        "user_id": "#961:335",
        "time": "2019-12-18 10:26:05"
      },
      "org_unit_id": "#999:14",
      "time_rc": "2019-12-18 10:25:49"
    },
    {
      "id": "#1185:3247",
      "class_name": "RcHorm",
      "patient_id": "#71:40788",
      "ehr_id": "#873:43666",
      "published": {
        "user_id": "#961:335",
        "time": "2019-12-18 10:27:21"
      },
      "org_unit_id": "#999:14",
      "time_rc": "2019-12-17 10:26:08",
      "rc_horm": {
        "time_rc_in": "2019-12-17",
        "org_unit_id": "#999:14",
        "kind": {
          "pharm": true
        },
        "aim": {
          "id": "1",
          "code": "PRIMARY",
          "caption": "при лечении первичной опухоли"
        },
        "condition": {
          "id": "1",
          "code": "AMB",
          "caption": "амбулаторно"
        },
        "drugs": [
          {
            "drug": {
              "orid": "#1550:61",
              "name": "бикалутамид",
              "type": {
                "id": "2",
                "code": "HT",
                "caption": "гормонотерапия"
              },
              "code": "Ю008"
            },
            "dose": 150.0,
            "unit": {
              "id": "2",
              "code": "MG",
              "caption": "мг"
            }
          }
        ]
      }
    }
  ]
}
```
