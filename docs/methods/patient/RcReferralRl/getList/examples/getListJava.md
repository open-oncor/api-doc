[Работа с пациентами](../../../index.md)
=====================================

### ![GET](../../../../../img/get.png) [/patient/RcReferralRL/getList`?patient_id={patient_id}`](../index.md)

### Java пример

```java
public class GetList {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = client.getPatient("70:33669");

        List<Records.Rc> patientRcReferralRLList = client.getPatientRcReferralRLList(patient.getId());

        Records.Rc rc = patientRcReferralRLList.get(0);
        String id = rc.getId();
    }
}
```

**[HTTP примеры](getList.md)**