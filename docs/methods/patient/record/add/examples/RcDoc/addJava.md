### Добавление медицинской записи пациенту (RcDoc)
### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

```java
public class AddRcDoc {
    private void addRcDoc() throws  IOException {
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        client.addPatientRecord(Records.Rc.newBuilder()
                .setPatientId(newPatient.getId())
                .setTimeRc(dateFormat.format(new Date()))
                .setRcDoc(Records.Rc.RcDoc.newBuilder()
                        .setCategory("лечение")
                        .setHtml("<body><h1>Протокол химиотерапии</h1>Данные протокола находятся здесь</body>")
                )
                .build());
    }
}
```

