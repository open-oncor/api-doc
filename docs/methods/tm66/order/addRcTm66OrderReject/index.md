## Передача документа "Отказ в проведении ДЭЗО"

### ![POST](../../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [RcTm66OrderReject](../../../../types/types.md#com.siams.med.api.Rc.RcTm66OrderReject)

Создает запись "Отказ в проведении ДЭЗО" (RcTm66OrderReject)

### Пример http

**Request**  
POST `http://dev.onco-reg.ru/api/1.0/json/tm66/order/addRcTm66OrderReject HTTP/1.1`

```json
{
    "record":{
        "rc_tm66_order_reject":{
            "order_id":"{{rcId}}",
            "reason":{
                "code":"ДАННЫЕ_ПАЦИЕНТА"
            },
            "text":"Не указан возраст",
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
     "id": "#1937:0",
     "class_name": "RcTm66OrderReject",
     "patient_id": "#65:9467",
     "ehr_id": "#1049:9467",
     "published": {
       "user_id": "#961:97",
       "time": "2020-05-08 10:01:51"
     },
     "org_unit_id": "#999:28",
     "time_rc": "2020-05-08 10:01:51",
     "rc_tm66_order_reject": {
       "order_id": "#1929:0",
       "reason": {
         "id": "1",
         "code": "ДАННЫЕ_ПАЦИЕНТА",
         "caption": "Недостаточно данных о пациенте"
       },
       "text": "Не указан возраст",
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