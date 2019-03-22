## Добавление статистической записи 'Регистрация смерти' (RcDeath) указанному пациенту 

### ![POST](../../../../../img/post.png) /patient/record/add
* **Request:** [RcDeath](../../../../../types/types.md#com.siams.med.api.Rc.RcDeath) **record** <patient_id, RcDeath>
* **Response:** [[RcDeath](../../../../../types/types.md#com.siams.med.api.Rc.RcDeath)]

Статистическая запись 'Регистрация смерти' добавляется как запись Rc указанному пациенту.

### Пример http 

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#67:34043",
        "rc_death":{
            "reason":{
                "orid":"#846:150",
                "code":"C50",
                "caption":"Злокачественное новообразование молочной железы"
            },
            "autopsy":{
                "id":"0"
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
            "id":"#1074:16805",
            "class_name":"RcDeath",
            "patient_id":"#67:34043",
            "ehr_id":"#1051:34043",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-10 09:50:00"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-10 09:50:00",
            "rc_death":{
                "reason":{
                    "orid":"#846:150",
                    "code":"C50",
                    "caption":"Злокачественное новообразование молочной железы"
                },
                "autopsy":{
                    "orid":"#149:0",
                    "id":"0",
                    "caption":"неизвестно, проводилась ли"
                }
            }
        }
    ]
}
```


### Пример java

```java
public class AddRcDeath {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Records.Rc rc = client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(patient.getId())
                .setRcDeath(Records.Rc.RcDeath.newBuilder()
                        .setReason(Directories.RBiMKB308.newBuilder().setCode("C50")))
                .build());

        Records.Rc.RcDeath RcDeath = rc.getRcDeath();
    }
}
```

