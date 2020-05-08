## Передача экспертизы качества ервичного протокола исследования

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderExpertiseProtocol](../../../../types/types.md##com.siams.med.api.Rc.RcTm66OrderExpertiseProtocol)  
* **Response:** [RcTm66OrderExpertiseProtocol](../../../../types/types.md##com.siams.med.api.Rc.RcTm66OrderExpertiseProtocol)  

Создает запись "Экспертиза качества первичного протокола исследования"

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
      "text": "не указан точный возраст пациента",
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
     "id": "#1905:0",
     "class_name": "RcTm66OrderExpertiseProtocol",
     "patient_id": "#65:9467",
     "ehr_id": "#1049:9467",
     "published": {
       "user_id": "#961:97",
       "time": "2020-05-08 09:54:24"
     },
     "org_unit_id": "#999:28",
     "time_rc": "2020-05-08 09:54:24",
     "rc_tm66_order_expertise_protocol": {
       "order_id": "#1929:0",
       "result": {
         "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
         "caption": "Выявлены незначительные нарушения, не влияющие на сформированное заключение"
       },
       "text": "не указан точный возраст пациента",
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
message RcTm66OrderExpertiseProtocol {
        optional string order_id = 1; // id записи RcTm66Order Заявка на ДЭЗО
        optional Tm66ExpertProtocolResult result = 2; // Тип результата экспертизы первичного протокола
        optional string text = 3; // Дополнительная информация
        optional MedResource expert = 10; // Исполнитель
        optional MedDepart expert_d = 11; // Отделение исполнителя
        optional MO expert_m_o = 12; // МО исполнителя
    }
```