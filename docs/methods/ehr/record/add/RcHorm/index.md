## Добавление статистической записи 'Гормонотерапия' в указанное заболевание (RcHorm)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcHorm](../../../../../types/types.md#com.siams.med.api.Rc.RcHorm) **record** <patient_id, ehr_id, RcHorm>
* **Response:** [[RcHorm](../../../../../types/types.md#com.siams.med.api.Rc.RcHorm)]

Статистическая запись 'Гормонотерапия' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#67:33340",
        "ehr_id":"#874:36231",
        "rc_horm":{
            "time_rc_in":"2018-10-04 23:54:05",
            "time_rc_out":"2018-10-04 23:54:05",
            "kind":{
                "xrt":true
            },
            "aim":{
                "code":"NONE"
            },
            "condition":{
                "code":"NONE"
            },
            "compl":{
                "id":"1"
            },
            "drugs":[
                {
                    "drug":{
                        "code":"Ю001"
                    },
                    "dose":123.0,
                    "unit":{
                        "code":"MKG"
                    }
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
            "id":"#1185:2310",
            "class_name":"RcHorm",
            "patient_id":"#67:33340",
            "ehr_id":"#874:36231",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:54:05"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:54:05",
            "rc_horm":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```



### Пример java

```java
public class AddRcHorm {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcHorm(Records.Rc.RcHorm.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Records.Rc.RcHorm.Kind.newBuilder().setXrt(true))
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .addDrugs(Directories.DrugRecord.newBuilder()
                                .setDrug(Directories.Drug.newBuilder().setCode("Ю001"))
                                .setUnit(Directories.DoseUnit.newBuilder().setCode("MKG"))
                                .setDose(123.0)
                        )
                )
                .build()
        );

        String id = newRecord.getId();
        Records.Rc.RcHorm rcHorm = newRecord.getRcHorm();
    }
}

```

<!--- todo добавить описание как выбрать препарат -->