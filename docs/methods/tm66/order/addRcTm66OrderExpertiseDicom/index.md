## Добавить экспертизу качества DICOM

### ![POST](../../../../img/post.png) /tm66/order/addRcTm66OrderExpertiseDicom
* **Request:** [RcTm66OrderExpertiseDicom](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderExpertiseDicom)
* **Response:** [RcTm66OrderExpertiseDicom](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderExpertiseDicom)  

Создает запись "Экспертиза качества DICOM"

### Структура сообщения ProtoBuffer
```proto
 message RcTm66OrderExpertiseDicom {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ExpertDicomResult result = 2; // Тип значимости экспертизы качества выполнения рентген-радиологического снимка
        optional string description = 3; // Краткое описание
        optional string pdf_id = 4; // Документ в формате PDF (Attachment.id)
        optional string pdf_ds_id = 5; // Открепленная ЭЦП PDF документа (Attachment.id)
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
    }


/**
 * Запись справочника "Тип значимости экспертизы качества выполнения рентген-радиологического снимка"
 * * НАРУШЕНИЙ_НЕТ("Нарушений нет"),
 * * НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ("Выявлены незначительные нарушения, обусловленные оборудованием, на котором проводилось исследование"),
 * * ЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ("Выявленные значительные нарушения, не позволяющие сделать достоверные заключения")
*/
message Tm66ExpertDicomResult {
    optional string code = 3;
    optional string caption = 4;
}

/**
 * Запись справочника "Врач"
*/
message MedResource {
    optional string id = 2;
    optional string code = 3;
    repeated string date_range = 5;

    optional string name = 7;
    optional string doctor_code = 8;
    optional string doctor_name = 9;
    optional string med_org_code = 10;
    optional string med_spec_code = 11;
}

/**
 * Запись справочника "Отделение"
*/
message MedDepart {
    optional string id = 2;
    optional string code = 3;
    repeated string date_range = 5;

    optional string name = 7;
    optional string depart_code = 8;
    optional string med_org_code = 9;
    optional string name_full = 10;
    optional string name_short = 11;
    optional string type_help = 12;
}
```

### Пример http

**Request**   

POST `https://demo.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderExpertiseDicom HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

```json
{
    "record":{
        "rc_tm66_order_expertise_dicom":{
            "order_id":"{{rcId}}",
            "result":{
                "code":"НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ"
            },
            "description": "не указаны параметры оборудования",
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
      "id": "#1977:1",
      "class_name": "RcTm66OrderExpertiseDicom",
      "patient_id": "#69:111",
      "ehr_id": "#1053:111",
      "published": {
        "user_id": "#962:222",
        "time": "2020-05-18 20:44:45"
      },
      "org_unit_id": "#993:29",
      "time_rc": "2020-05-18 20:44:45",
      "rc_tm66_order_expertise_dicom": {
        "order_id": "#1930:0",
        "result": {
          "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
          "caption": "Выявлены незначительные нарушения, обусловленные оборудованием, на котором проводилось исследование"
        },
        "description": "не указаны параметры оборудования",
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
