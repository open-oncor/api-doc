## Добавление статистической записи 'Лучевая терапия' в указанное заболевание (RcRay)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcRay](../../../../../types/types.md#com.siams.med.api.Rc.RcRay) **record** <patient_id, ehr_id, RcRay>
* **Response:** [[RcRay](../../../../../types/types.md#com.siams.med.api.Rc.RcRay)]

Статистическая запись 'Лучевая терапия' добавляется как запись Rc в указанное заболевание.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`

```json
{
    "record":{
        "patient_id":"#68:33232",
        "ehr_id":"#875:36094",
        "rc_ray":{
            "time_rc_in":"2018-10-04 23:59:53",
            "time_rc_out":"2018-10-04 23:59:53",
            "aim":{
                "code":"NONE"
            },
            "kind":{
                "code":"NONE"
            },
            "method":{
                "code":"NONE"
            },
            "way":{
                "code":"NONE"
            },
            "radio":{
                "code":"NONE"
            },
            "doze":1.0,
            "doze_meta":1.0,
            "condition":{
                "code":"NONE"
            },
            "compl":{
                "id":"1"
            },
            "session_count":1,
            "srv":[
                {
                    "code":"SRV_3_1_1"
                }
            ]
        }
    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#1275:8662",
            "class_name":"RcRay",
            "patient_id":"#68:33232",
            "ehr_id":"#875:36094",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:59:53"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:59:53",
            "rc_ray":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```


### Пример java

```java
public class AddRcRay {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        final ProtoBuffClient client = newProtoBuffClient();
        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcRay(Records.Rc.RcRay.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Directories.RayKind.newBuilder().setCode("NONE"))
                        .setMethod(Directories.RayMethod.newBuilder().setCode("NONE"))
                        .setWay(Directories.RayWay.newBuilder().setCode("NONE"))
                        .setRadio(Directories.RayRadio.newBuilder().setCode("NONE"))
                        .setDoze(1f)
                        .setDozeMeta(1f)
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .setSessionCount(1)
                        .addSrv(Directories.Srv59Ray.newBuilder().setCode("SRV_3_1_1"))
                )
                .build()
        );

        String id = newEhrRecord.getId();
        Records.Rc.RcRay rcRay = newEhrRecord.getRcRay();
    }
}
```

