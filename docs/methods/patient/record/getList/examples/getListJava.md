[Работа с пациентами](../../../index.md)
==================================

### ![GET](../../../../../img/get.png) [/patient/record/getList`?patient_id={patient_id}`](../index.md)

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

**[HTTP примеры](getList.md)**