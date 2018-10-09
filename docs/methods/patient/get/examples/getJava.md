### Получение данных пациента по его ключу (java)

### ![GET](../../../../img/get.png) [/patient/get`?id={patient_id}`](../index.md)

```java
class GetPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();
        Patients.Patient patient = client.getPatient("70:33669");
        
        String id = patient.getId();
        String code = patient.getCode();
    }
}
```

