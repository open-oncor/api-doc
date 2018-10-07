[Работа с пациентами](../index.md)
==================================

### ![GET](../../../../img/get.png) [/patient/get`?id={patient_id}`](../index.md)

```java
class GetPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();
        client.getPatient("65:33650");
    }
}
```

**[HTTP примеры кода](get.md)**