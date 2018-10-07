[Работа с пациентами](../../../index.md)
==================================

### ![GET](../../../../../img/get.png) [/patient/record/getList`?patient_id={patient_id}`](../index.md)

```java
public class GetPatientRcList {
    public static void main(String[] args) throws IOException {
        newProtoBuffClient().getPatientRecords("65:33650");
    }
}
```

**[HTTP примеры](getList.md)**