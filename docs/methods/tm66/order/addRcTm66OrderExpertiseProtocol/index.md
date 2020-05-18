## Передача экспертизы качества первичного протокола исследования

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderExpertiseProtocol](../../../../types/types.md##com.siams.med.api.Rc.RcTm66OrderExpertiseProtocol)  
* **Response:** [RcTm66OrderExpertiseProtocol](../../../../types/types.md##com.siams.med.api.Rc.RcTm66OrderExpertiseProtocol)  

Создает запись "Экспертиза качества первичного протокола исследования"

### Структура сообщения ProtoBuffer
```proto
 message RcTm66OrderExpertiseProtocol {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ExpertProtocolResult result = 2; // Тип значимости экспертизы качества протокола
        optional string description = 3; // Краткое описание
        optional string pdf_id = 4; // Документ в формате PDF (Attachment.id)
        optional string pdf_ds_id = 5; // Открепленная ЭЦП PDF документа (Attachment.id)
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
    }
```

### Пример http

**Request**   

POST `http://dev.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderExpertiseProtocol HTTP/1.1`
```json
{
    "record":{
        "rc_tm66_order_expertise_protocol":{
            "order_id":"{{rcId}}",
            "result":{
                "code":"НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ"
            },
            "description": "не указан точный возраст пациента",
            "pdf_id": "{{attachmentId}}",
            "pdf_ds_id": "{{attachmentId}}",
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
      "id": "#1969:1",
      "class_name": "RcTm66OrderExpertiseProtocol",
      "patient_id": "#69:111",
      "ehr_id": "#1053:111",
      "published": {
        "user_id": "#962:222",
        "time": "2020-05-18 20:44:00"
      },
      "org_unit_id": "#993:29",
      "time_rc": "2020-05-18 20:44:00",
      "rc_tm66_order_expertise_protocol": {
        "order_id": "#1930:0",
        "result": {
          "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
          "caption": "Выявлены незначительные нарушения, не влияющие на сформированное заключение"
        },
        "description": "не указан точный возраст пациента",
        "pdf_id": "#1587:4385",
        "pdf_ds_id": "#1587:4385",
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
