### Получение списка медицинских записей пациента для указанного заболевания (http)

### ![GET](../../../../img/get.png) [/rc/getList`?ehr_id={ehr_id}`](../index.md)

**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/rc/getList?ehr_id=1054:29080 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "id":"#1062:39222",
            "class_name":"RcRegIn",
            "patient_id":"#70:29080",
            "ehr_id":"#1054:29080",
            "published":{
                "user_id":"#962:7",
                "time":"2017-08-03 20:34:03"
            },
            "org_unit_id":"#993:41",
            "time_rc":"2017-08-03 00:00:00",
            "rc_reg_in":{
                "clause":{
                    "id":"2",
                    "code":"RI_A2",
                    "caption":"при жизни повторно"
                }
            }
        },
        {
             "id":"#1081:12558",
             "class_name":"RcClinicalGroup",
             "patient_id":"#70:29080",
             "ehr_id":"#1054:29080",
             "published":{
                 "user_id":"#961:159",
                 "time":"2018-08-08 08:13:18"
             },
             "org_unit_id":"#999:28",
             "time_rc":"2018-06-06 08:13:04",
             "rc_clinical_group":{
                 "group_type":{
                     "id":"3",
                     "code":"II",
                     "caption":"II"
                 }
             }
        }
    ]
}
```
