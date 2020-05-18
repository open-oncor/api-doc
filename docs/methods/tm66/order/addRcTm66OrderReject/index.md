## Передача документа "Отказ в проведении ДЭЗО"

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderReject](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderReject)
* **Response:** [RcTm66OrderReject](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderReject)

Создает запись "Отказ в проведении ДЭЗО"

### Структура сообщения ProtoBuffer

```proto
message RcTm66OrderReject {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66OrderRejectReason reason = 2; // Причины отказа проведения ДЭЗО
        optional string description = 3; // Краткое описание
        optional string pdf_id = 4; // Документ в формате PDF (Attachment.id)
        optional string pdf_ds_id = 5; // Открепленная ЭЦП PDF документа (Attachment.id)
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
    }
```

### Пример http

**Request**  
POST `http://dev.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderReject HTTP/1.1`

```json
{
    "record":{
        "rc_tm66_order_reject":{
            "order_id":"#1937:2",
            "reason":{
                "code":"ДАННЫЕ_ПАЦИЕНТА"
            },
            "description":"Не указан возраст",
            "expert":{
                "id": "39115-661768-26(20190905)"
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
        "id": "#1937:5",
        "class_name": "RcTm66OrderReject",
        "patient_id": "#69:111",
        "ehr_id": "#1053:111",
        "published": {
          "user_id": "#962:222",
          "time": "2020-05-18 20:40:23"
        },
        "org_unit_id": "#993:29",
        "time_rc": "2020-05-18 20:40:23",
        "rc_tm66_order_reject": {
          "order_id": "#1930:0",
          "reason": {
            "id": "1",
            "code": "ДАННЫЕ_ПАЦИЕНТА",
            "caption": "Недостаточно данных о пациенте"
          },
          "description": "Не указан возраст",
          "expert": {
            "id": "39115-661768-26(20190905)",
            "code": "39115-661768-26",
            "date_range": [
              "20190905",
              "29991231"
            ],
            "name": "НОВОСЕЛОВА О О",
            "doctor_code": "39115",
            "doctor_name": "НОВОСЕЛОВА О О",
            "med_org_code": "661768",
            "med_spec_code": "26"
          }
        }
      }
    ]
}
```