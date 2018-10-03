# [Сценарии](../index.md)

## Выгрузка данных проведенного лечения из МИС МО в ОНКОР

1. [/patient/add](../../methods/patient/add/examples/add.md) `добавление нового пациента в ОНКОР` или
[/patient/search](../../methods/patient/search/examples/search.md) `поиск пациента`
2. [/ehr/add](../../methods/ehr/add/examples/add.md) `добавление ЭМЗ пациенту`
3. [/ehr/record/add](../../methods/ehr/record/add/examples/add.md) `добавление записи в ЭМЗ`

**Java example**
```java
public class NewRcRay {
    public static void main(String[] args) throws IOException {
        final RcDzTest rcDzTest = new RcDzTest();
        final Records.Rc ehrRecord = rcDzTest.addEhrRecord();
        final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        rcDzTest.client.addEhrRecord(Records.Rc.newBuilder()
                .setPatientId(ehrRecord.getPatientId())
                .setEhrId(ehrRecord.getEhrId())
                .setRcRay(Records.Rc.RcRay.newBuilder()
                        .setTimeRcIn(dateFormat.format(new Date()))
                        .setTimeRcOut(dateFormat.format(new Date()))
                )
                .build()
        );
    }
}

```