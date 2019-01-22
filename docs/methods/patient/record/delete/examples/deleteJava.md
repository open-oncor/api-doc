### Удаление записи из указанного пациента
### ![POST](../../../../../img/post.png) [/patient/record/delete](../index.md)

```java
class Demo {
    public static void main(String... args) { 
        client.deletePatientRecord(Records.Rc.newBuilder()
                .setId(ptnRc.getId())
                .setPatientId(ptnRc.getPatientId())
                .build());
    }
}
```

