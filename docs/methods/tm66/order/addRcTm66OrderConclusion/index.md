## Передача заключения ДЭЗО

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderConclusion](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderConclusion)
* **Response:** [RcTm66OrderConclusion](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderConclusion)

Создает запись "Заключение ДЭЗО".   
- RcTm66OrderConclusion.conclusion - `тип заключения из справочника Tm66ConclusionType`   
- RcTm66OrderConclusion.description - `Значимое текстовое поле из документа, например, "результатирующая" часть из документа или пользовательский текст`  
- RcTm66OrderConclusion.pdf_id - `Attachment.id предварительно загруженного API-методом attachment/create PDF-файла документа заключения `
- RcTm66OrderConclusion.pdf_ds_id - `Attachment.id предварительно загруженного API-методом attachment/create файла открепленной цифроой подписи файла pdf_id`  

### Структура сообщения ProtoBuffer
```proto
 message RcTm66OrderConclusion {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ConclusionType conclusion = 2; // Тип заключения
        optional string description = 3; // Краткое описание
        optional string pdf_id = 4; // Документ в формате PDF (Attachment.id)
        optional string pdf_ds_id = 5; // Открепленная ЭЦП PDF документа (Attachment.id)
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
    }
```

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
        "id": "#1953:1",
        "class_name": "RcTm66OrderConclusion",
        "patient_id": "#69:111",
        "ehr_id": "#1053:111",
        "published": {
          "user_id": "#962:222",
          "time": "2020-05-18 20:42:45"
        },
        "org_unit_id": "#993:29",
        "time_rc": "2020-05-18 20:42:45",
        "rc_tm66_order_conclusion": {
          "order_id": "#1930:0",
          "conclusion": {
            "code": "ЗАКЛЮЧЕНИЕ_СОВПАДАЕТ",
            "caption": "Заключение эксперта совпадает с направленным заключением"
          },
          "description": "Заключение полностью совпадает",
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
