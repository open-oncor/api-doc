## Получение списка медицинских записей общих для пациента (не привязанных к конретному заболеванию)


### ![GET](../../../../img/get.png) /patient/record/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../../types/types.md#com.siams.med.api.Rc)]

Возвращает список записей для пациента с идентификатором [patient_id](../../../../types/types.md#com.siams.med.api.Rc).

В ответе передаётся массив объектов [Rc](../../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/patient/record/getList?patient_id=70:33669 HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"#1060:45958",
            "class_name":"RcRegIn",
            "patient_id":"#70:33669",
            "ehr_id":"#1054:33669",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:27:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:27:53",
            "rc_reg_in":{
                "clause":{
                    "code":"NONE",
                    "caption":"неизвестно"
                }
            }
        },
        {
            "id":"#1068:19100",
            "class_name":"RcRegOut",
            "patient_id":"#70:33669",
            "ehr_id":"#1054:33669",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-08 23:27:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-08 23:27:53",
            "rc_reg_out":{
                "reason":{
                    "code":"NONE",
                    "caption":""
                }
            }
        }
    ]
}
```

### Пример java

```java
public class GetPatientRcList {
    public static void main(String[] args) throws IOException {
        List<Records.Rc> patientRecords = newProtoBuffClient().getPatientRecords("70:33669");
        Records.Rc rc = patientRecords.get(0);
        
        String id = rc.getId();
        String ehrId = rc.getEhrId();
    }
}
```