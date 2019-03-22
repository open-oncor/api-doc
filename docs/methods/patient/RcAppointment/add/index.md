##Добавление предварительной записи пациента на приём


### ![POST](../../../../img/post.png) /patient/RcAppointment/add
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) record
* **Response:** [Rc](../../../../types/types.md#com.siams.med.api.Rc)

Добавляет предварительную запись. В запросе передаётся объект - [Rc](../../../../types/types.md#com.siams.med.api.Rc). 

В ответе - [Rc](../../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/RcAppointment/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#70:33669",
        "rc_appointment":{
            "rc_referral_id":"#1505:3512",
            "confirmed":false,
            "note":"Example"
        }
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#1089:3142",
            "class_name":"RcAppointment",
            "patient_id":"#70:33669",
            "ehr_id":"#876:36710",
            "published":{
                "user_id":"#961:170",
                "time":"2018-10-09 00:54:18"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-09 00:54:18",
            "rc_appointment":{
                "rc_referral_id":"#1505:3512",
                "confirmed":false,
                "note":"Example"
            }
        }
    ]
}
```


### Пример Java

```java
class AddPatientRcAppointment {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = client.getPatient("70:33669");

        final List<Records.Rc> rcReferralList = client.getPatientRcReferralRLList(patient.getId());
        for (Records.Rc rc : rcReferralList) {
            final Records.Rc.RcReferral rcReferral = rc.getRcReferral();
            if (!rcReferral.hasRcAppointmentId()) {
                TestUtils.print(patient);
                final Records.Rc rcAppointment = client.addPatientRcAppointment(Records.Rc.newBuilder()
                        .setPatientId(patient.getId())
                        .setRcAppointment(Records.Rc.RcAppointment.newBuilder()
                                .setRcReferralId(rc.getId())
                                .setConfirmed(false)
                                .setNote("Example")
                        )
                        .build());
                TestUtils.print(rcAppointment);
            }
        }
    }
}

```