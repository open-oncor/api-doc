## Добавление направления в указанное заболевание (RcReferral)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcReferral](../../../../../types/types.md#com.siams.med.api.Rc.RcReferral) **record** <patient_id, ehr_id, RcReferral>
* **Response:** [[RcReferral](../../../../../types/types.md#com.siams.med.api.Rc.RcReferral)]

Направление добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#66:6375",
        "ehr_id":"#879:6697",
        "rc_referral":{
            "purpose":"Цель направления",
            "routing_list":{
                "apply_last_on_any_other_disease_date":"2018-02-01",
                "apply_last_date":"2018-02-01",
                "apply_first_date":"2018-02-01",
                "request_date":"2018-02-01",
                "admission_date":"2018-02-01",
                "examination_lsat_date":"2018-02-01",
                "treatment_first_date":"2018-02-01",
                "expert_opinion":"Экспертное заключение",
                "expert_opinion_date":"2018-02-01",
                "note":"Примечание к направлению",
                "diagnostics":[
                    {
                        "type":{
                            "code":"OAM"
                        },
                        "date":"2018-01-01",
                        "note":"Примечание к обследованию"
                    }
                ]
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
      "id": "#1506:0",
      "class_name": "RcReferralRL",
      "patient_id": "#66:6375",
      "ehr_id": "#879:6697",
      "published": {
        "user_id": "#962:0",
        "time": "2018-12-18 10:47:45"
      },
      "org_unit_id": "#993:0",
      "time_rc": "2018-12-18 10:47:44",
      "rc_referral": {
        "referral_type": "RF_CONSULT",
        "purpose": "Цель направления",
        "routing_list": {
          "apply_last_on_any_other_disease_date": "2018-02-01 00:00:00",
          "apply_last_date": "2018-02-01 00:00:00",
          "apply_first_date": "2018-02-01 00:00:00",
          "request_date": "2018-02-01 00:00:00",
          "admission_date": "2018-02-01 00:00:00",
          "examination_lsat_date": "2018-02-01 00:00:00",
          "treatment_first_date": "2018-02-01 00:00:00",
          "health_record_code": "",
          "expert_opinion": "Экспертное заключение",
          "expert_opinion_date": "2018-02-01 00:00:00",
          "note": "Примечание к направлению",
          "referral_code": "1000002",
          "diagnosis": {
            "mkb_code": "C50.4",
            "mkb_name": "Верхненаружного квадранта молочной железы",
            "tnm": {
              "t": {
                "id": "6",
                "code": "T_1A",
                "caption": "1a"
              },
              "n": {
                "id": "2",
                "code": "N_0",
                "caption": "0"
              },
              "m": {
                "id": "2",
                "code": "M_0",
                "caption": "0"
              },
              "g": {
                "code": "NONE",
                "caption": ""
              }
            },
            "dz_stage": {
              "id": "4",
              "code": "I",
              "caption": "I"
            },
            "how_discover": {
              "orid": "#291:0",
              "id": "1",
              "caption": "обратился сам"
            },
            "morph_class": {
              "orid": "#855:30",
              "code": "8500/3",
              "caption": "8500/3. Инфильтрирующий протоковый рак"
            },
            "tumor_main": {
              "orid": "#340:0",
              "id": "1",
              "caption": "основная"
            },
            "tumor_side": {
              "orid": "#347:0",
              "id": "1",
              "caption": "слева"
            },
            "plural": {
              "orid": "#307:0",
              "id": "1",
              "caption": "нет"
            }
          },
          "diagnostics": [
            {
              "type": {
                "code": "OAM",
                "caption": "ОАМ"
              },
              "date": "2018-01-01 00:00:00",
              "note": "Примечание к обследованию"
            }
          ]
        }
      }
    }
  ]
}
```

### Пример java

```java
public class AddRcReferral {
    public static void main(String[] args) throws IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

        ProtoBuffClient client = newProtoBuffClient();

        final Records.Rc ehrDzRecord = getEhrDzRecord();

        Records.Rc newEhrRecord = rcDzTest.client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrRecord.getPatientId())
                .setEhrId(ehrRecord.getEhrId())
                .setRcReferral(Records.Rc.RcReferral.newBuilder()
                        .setPurpose("Цель направления")
                        .setRoutingList(Routing.RoutingList.newBuilder()
                                .setAdmissionDate("2018-02-01")
                                .setApplyFirstDate("2018-02-01")
                                .setApplyLastDate("2018-02-01")
                                .setApplyLastOnAnyOtherDiseaseDate("2018-02-01")
                                .setRequestDate("2018-02-01")
                                .setExaminationLsatDate("2018-02-01")
                                .setTreatmentFirstDate("2018-02-01")
                                .setExpertOpinionDate("2018-02-01")
                                .setExpertOpinion("Экспертное заключение")
                                .addDiagnostics(Routing.RoutingList.Diagnostics.newBuilder()
                                        .setType(Directories.DiagnosticsType.newBuilder().setCode("OAM"))
                                        .setDate("2018-01-01")
                                        .setNote("Примечание к обследованию"))
                                .setNote("Примечание к направлению")
                        )
                )
                .build()
        );

    }
}

```
