## Получение списка заболеваний пациента

### ![GET](../../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../types/types.md#com.siams.med.api.EHR)
* **Response:** [[EHR](../../../types/types.md#com.siams.med.api.EHR)]

Возвращает список заболеваний пациента по ключу пациента.


### Пример http

**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/ehr/getList?patient_id=71:40788 HTTP/1.1`
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**

```json
{
  "result": [
    {
      "id": "#873:43666",
      "patient_id": "#71:40788",
      "summary": "",
      "dz": {
        "mkb_code": "C61",
        "mkb_name": "Злокачественное новообразование предстательной железы",
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
        "dz_stage": {
          "id": "8",
          "code": "II",
          "caption": "II"
        },
        "how_discover": {
          "orid": "#291:0",
          "id": "1",
          "caption": "обратился сам"
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
        "plural": {
          "orid": "#307:0",
          "id": "1",
          "caption": "нет"
        }
      }
    },
    {
      "id": "#879:47719",
      "patient_id": "#71:40788",
      "summary": "",
      "dz": {
        "mkb_code": "C20",
        "mkb_name": "Злокачественное новообразование прямой кишки",
        "tnm": {
          "t": {
            "code": "NONE",
            "caption": ""
          },
          "n": {
            "code": "NONE",
            "caption": ""
          },
          "m": {
            "code": "NONE",
            "caption": ""
          },
          "g": {
            "code": "NONE",
            "caption": ""
          }
        },
        "dz_stage": {
          "code": "NONE",
          "caption": ""
        },
        "how_discover": {
          "orid": "#291:0",
          "id": "1",
          "caption": "обратился сам"
        },
        "morph_class": {
          "orid": "#849:11",
          "code": "8144/3",
          "caption": "8144/3. Аденокарцинома кишечного типа"
        }
      }
    },
    {
      "id": "#874:50327",
      "patient_id": "#71:40788",
      "summary": ""
    }
  ]
}
```


