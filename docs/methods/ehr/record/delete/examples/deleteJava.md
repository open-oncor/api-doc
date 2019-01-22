### Удаление записи из указанного заболевания
### ![POST](../../../../../img/post.png) [/ehr/record/delete](../index.md)

```java
class Demo {
    public static void main(String... args) { 
        client.deleteEhrRecord(Records.Rc.newBuilder()
                               .setId(edrRc.getId())
                               .setPatientId(edrRc.getPatientId())
                               .setEhrId(edrRc.getEhrId())
                               .build());
    }
}
```

