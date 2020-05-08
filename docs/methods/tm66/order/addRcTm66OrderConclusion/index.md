## Передача заключения ДЭЗО

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderConclusion](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderConclusion)
* **Response:** [RcTm66OrderConclusion](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderConclusion)

Создает запись "Заключение ДЭЗО"

### Пример http

**Request** 
 
POST `http://dev.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderConclusion HTTP/1.1`
```json
{
    "record":{
        "rc_tm66_order_conclusion":{
            "order_id":"{{rcId}}",
            "conclusion_type":{
                "code":"ЗАКЛЮЧЕНИЕ_СОВПАДАЕТ"
            },
            "conclusion": "Заключение полностью совпадает",
            "conclusion_pdf_id": "{{attachmentId}}",
            "conclusion_pdf_ds_id": "{{attachmentId}}",
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
     "id": "#1961:0",
     "class_name": "RcTm66OrderConclusion",
     "patient_id": "#65:9467",
     "ehr_id": "#1049:9467",
     "published": {
       "user_id": "#961:97",
       "time": "2020-05-08 10:02:44"
     },
     "org_unit_id": "#999:28",
     "time_rc": "2020-05-08 10:02:44",
     "rc_tm66_order_conclusion": {
       "order_id": "#1929:0",
       "conclusion_type": {
         "code": "ЗАКЛЮЧЕНИЕ_СОВПАДАЕТ",
         "caption": "Заключение эксперта совпадает с направленным заключением"
       },
       "conclusion": "Заключение полностью совпадает",
       "conclusion_pdf_id": "#1585:4325",
       "conclusion_pdf_ds_id": "#1585:4325",
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
### Структура сообщения ProtoBuffer
```proto
    message RcTm66OrderConclusion {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ConclusionType conclusion_type = 2; // Тип заключения
        optional string conclusion = 3; // Заключение
        optional string conclusion_pdf_id = 4; // Заключение в формате PDF (Attachment.id)
        optional string conclusion_pdf_ds_id = 5; // Открепленная ЭЦП заключения PDF (Attachment.id)
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
    }
```

