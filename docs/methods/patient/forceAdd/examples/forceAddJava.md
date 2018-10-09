[Работа с пациентами](../index.md)
==================================
**[http](examples/forceAdd.md)**
**java**

### ![GET](../../../../img/get.png) [/patient/forceAdd](../index.md)

```java
class AddPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        client.forceAddPatient(Patients.Patient.newBuilder()
                .setFirstName("Сергеев")
                .setMiddleName("Сергей")
                .setLastName("Сергеевич")
                .setBirthDay("1977-01-01")
                .build());
    }
}
```