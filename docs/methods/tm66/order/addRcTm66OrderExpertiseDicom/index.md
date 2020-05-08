## Передача экспертизы качества DICOM

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderExpertiseDicom](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderExpertiseDicom)
* **Response:** [RcTm66OrderExpertiseDicom](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderExpertiseDicom)  

Создает запись "Экспертиза качества DICOM"

### Пример http

**Request**   

POST `http://dev.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderExpertiseDicom HTTP/1.1`
```json
{
  "record":{
    "rc_tm66_order_expertise_dicom":{
      "order_id":"{{rcId}}",
      "result":{
        "code":"НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ"
      },
      "description": "не указаны параметры оборудования",
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
     "id": "#1945:0",
     "class_name": "RcTm66OrderExpertiseDicom",
     "patient_id": "#65:9467",
     "ehr_id": "#1049:9467",
     "published": {
       "user_id": "#961:97",
       "time": "2020-05-08 09:57:10"
     },
     "org_unit_id": "#999:28",
     "time_rc": "2020-05-08 09:57:10",
     "rc_tm66_order_expertise_dicom": {
       "order_id": "#1929:0",
       "result": {
         "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
         "caption": "Выявлены незначительные нарушения, обусловленные оборудованием, на котором проводилось исследование"
       },
       "description": "не указаны параметры оборудования",
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
message RcTm66OrderExpertiseDicom {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ExpertDicomResult result = 2; // Тип результата экспертизы первичного протокола
        optional string text = 3; // Дополнительная информация
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
        optional MO expert_m_o = 12; // МО исполнителя
    }
```