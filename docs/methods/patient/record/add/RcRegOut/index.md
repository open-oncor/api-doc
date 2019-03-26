## Добавление статистической записи 'Снятие с учёта' (RcRegOut) указанному пациенту 

### ![POST](../../../../../img/post.png) /patient/record/add
* **Request:** [RcRegOut](../../../../../types/types.md#com.siams.med.api.Rc.RcRegOut) **record** <patient_id, RcRegOut>
* **Response:** [[RcRegOut](../../../../../types/types.md#com.siams.med.api.Rc.RcRegOut)]

Статистическая запись 'Снятие с учёта' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанному пациенту.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`

```json
{
    "record":{
        "patient_id":"#70:33669",
        "rc_reg_out":{
            "reason":{
                "code":"NONE"
            }
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1067:19219",
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
public class AddRcRegOut {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcRegOut(Records.Rc.RcRegOut.newBuilder()
                        .setReason(Directories.RegOutReason.newBuilder().setCode("NONE")))
                .build());

        Records.Rc.RcRegOut rcRegOut = rc.getRcRegOut();
        Directories.RegOutReason reason = rcRegOut.getReason();
    }
}
```

