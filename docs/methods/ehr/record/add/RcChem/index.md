## Добавление статистической записи 'Химиотерапия' в указанное заболевание (RcChem)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcChem](../../../../../types/types.md#com.siams.med.api.Rc.RcChem) **record** <patient_id, ehr_id, RcChem>
* **Response:** [[RcChem](../../../../../types/types.md#com.siams.med.api.Rc.RcChem)]

Статистическая запись 'Химиотерапия' добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#66:33485",
        "ehr_id":"#873:36390",
        "rc_chem":{
            "time_rc_in":"2018-10-04 23:52:33",
            "time_rc_out":"2018-10-04 23:52:33",
            "aim":{
                "code":"NONE"
            },
            "kind":{
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
                        "code":"Э001"
                    },
                    "dose":123.0,
                    "unit":{
                        "code":"MKG"
                    }
                }
            ],
            "srv":[
                {
                    "code":"SRV_4_1_1"
                }
            ]
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1122:17250",
            "class_name":"RcChem",
            "patient_id":"#66:33485",
            "ehr_id":"#873:36390",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-04 23:52:34"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-04 23:52:33",
            "rc_chem":{
                "time_rc_in":"2018-10-04",
                "time_rc_out":"2018-10-04"
            }
        }
    ]
}
```



### Пример java

```java
public class AddRcChem {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrDzRecord.getPatientId())
                .setEhrId(ehrDzRecord.getEhrId())
                .setRcChem(Records.Rc.RcChem.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                        .setAim(Directories.TherapyAim.newBuilder().setCode("NONE"))
                        .setKind(Directories.ChemKind.newBuilder().setCode("NONE"))
                        .setCondition(Directories.TherapyCond.newBuilder().setCode("NONE"))
                        .setCompl(Directories.DrNK0439.newBuilder().setId("1"))
                        .addDrugs(Directories.DrugRecord.newBuilder()
                                .setDrug(Directories.Drug.newBuilder().setCode("Э001"))
                                .setUnit(Directories.DoseUnit.newBuilder().setCode("MKG"))
                                .setDose(123.0)
                        )
                        .addSrv(Directories.Srv59Chem.newBuilder().setCode("SRV_4_1_1"))
                )
                .build()
        );

        String id = newEhrRecord.getId();
        Records.Rc.RcChem rcChem = newEhrRecord.getRcChem();
    }
}

```

<!--- todo добавить описание как выбрать препарат -->