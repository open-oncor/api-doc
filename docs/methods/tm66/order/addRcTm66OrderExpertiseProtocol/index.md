## Передача экспертизы качества ервичного протокола исследования

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
      "id": "#1969:0",
      "class_name": "RcTm66OrderExpertiseProtocol",
      "patient_id": "#71:16260",
      "ehr_id": "#1055:16260",
      "published": {
        "user_id": "#961:97",
        "time": "2020-05-10 09:20:48"
      },
      "org_unit_id": "#999:28",
      "time_rc": "2020-05-10 09:20:48",
      "rc_tm66_order_expertise_protocol": {
        "order_id": "#1929:0",
        "result": {
          "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
          "caption": "Выявлены незначительные нарушения, не влияющие на сформированное заключение"
        },
        "description": "не указан точный возраст пациента",
        "pdf_id": "#1585:4533",
        "pdf_ds_id": "#1585:4533",
        "expert": {
         "id": "39115-661768-26(20190905)",
         "code": "39115-661768-26",
         "dateRange": [
           "20190905",
           "29991231"
         ],
         "doctorCode": "39115",
         "doctorName": "НОВОСЕЛОВА О О",
         "medOrgCode": "661768",
         "medSpecCode": "26"
       }
     }
   }
 ]
}
```
