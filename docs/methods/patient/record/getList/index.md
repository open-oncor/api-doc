## Получение списка медицинских записей общих для пациента (не привязанных к конретному заболеванию)


### ![GET](../../../../img/get.png) /patient/record/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../../types/types.md#com.siams.med.api.Rc)]

Возвращает список записей для пациента с идентификатором [patient_id](../../../../types/types.md#com.siams.med.api.Rc).

В ответе передаётся массив объектов [Rc](../../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/patient/record/getList?patient_id=65:3583 HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

**Response**

```json
{
  "result": [
    {
      "id": "#1057:3583",
      "class_name": "RcRegIn",
      "patient_id": "#65:3583",
      "ehr_id": "#1049:3583",
      "published": {
        "user_id": "#968:9",
        "time": "2016-10-09 22:38:03"
      },
      "org_unit_id": "#993:41",
      "time_rc": "2005-02-01 00:00:00",
      "rc_reg_in": {
        "clause": {
          "id": "1",
          "code": "RI_A1",
          "caption": "при жизни впервые"
        }
      }
    },
    {
      "id": "#1070:2612",
      "class_name": "RcRegOut",
      "patient_id": "#65:3583",
      "ehr_id": "#1049:3583",
      "published": {
        "user_id": "#968:9",
        "time": "2016-10-09 22:38:03"
      },
      "org_unit_id": "#993:41",
      "time_rc": "2008-03-13 00:00:00",
      "rc_reg_out": {
        "reason": {
          "id": "4",
          "code": "RO_DIED_1",
          "caption": "умер от причин связанных с основным заболеванием"
        }
      }
    },
    {
      "id": "#1076:2060",
      "class_name": "RcDeath",
      "patient_id": "#65:3583",
      "ehr_id": "#1049:3583",
      "published": {
        "user_id": "#968:9",
        "time": "2016-10-09 22:38:03"
      },
      "org_unit_id": "#993:41",
      "time_rc": "2008-03-13 00:00:00",
      "rc_death": {
        "reason": {
          "orid": "#848:150",
          "code": "C50.1",
          "caption": "Центральной части молочной железы"
        },
        "autopsy": {
          "orid": "#147:0",
          "id": "2",
          "caption": "проводилась"
        }
      }
    }
  ]
}
```
