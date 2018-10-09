Добавление пациента (java)
=

### ![POST](../../../../img/post.png) [/patient/add](../index.md)

```java
class AddPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        client.addPatient(Patients.Patient.newBuilder()
                .setFirstName("Иван")
                .setMiddleName("Иванович")
                .setLastName("Иванов")
                .setBirthDay("1901-01-01")
                .setPhones("+7 911")
                .setGender(Directories.DrPrsG.newBuilder()
                        .setId("1")
                        .build())
                .build());

    }
}
```

