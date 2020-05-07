## Справочник Тип заключения ДЭЗО

### ![GET](../../../../img/get.png) /directory/get/Tm66ConclusionType
* **Response: [[Tm66ConclusionType](../../../../types/types.md#com.siams.med.api.Tm66ConclusionType)]**

### Пример http


**Request** 

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/Tm66ConclusionType HTTP/1.1`

**Response**

```json

{
  "result": [
    {
      "code": "ЗАКЛЮЧЕНИЕ_СОВПАДАЕТ",
      "caption": "Заключение эксперта совпадает с направленным заключением"
    },
    {
      "code": "ЗАКЛЮЧЕНИЕ_НЕ_СОВПАДАЕТ",
      "caption": "Заключение эксперта не совпадает с направленным заключением"
    },
    {
      "code": "ЗАКЛЮЧЕНИЕ_НЕ_СОВПАДАЕТ_КАРДИНАЛЬНО",
      "caption": "Заключение эксперта кардинально не совпадает с направленным заключением"
    },
    {
      "code": "ДИАГНОЗ_ПОДТВЕРЖДЕН",
      "caption": "Диагноз подтвержден"
    },
    {
      "code": "ДИАГНОЗ_УТОЧНЕН",
      "caption": "Уточнение диагноза"
    },
    {
      "code": "ДИАГНОЗ_НЕ_ПОДТВЕРЖДЕН",
      "caption": "Диагноз не подтвержден"
    },
    {
      "code": "ИЗМЕНЕНИЕ_ТАКТИКИ_НЕ_ТРЕБУЕТСЯ",
      "caption": "Изменение тактики лечения не требуется"
    },
    {
      "code": "ИЗМЕНЕНИЕ_ТАКТИКИ_ТРЕБУЕТСЯ",
      "caption": "Требуется изменение тактики лечения"
    },
    {
      "code": "ВМЕШАТЕЛЬСТВО_ТРЕБУЕТСЯ",
      "caption": "Требуется проведение оперативного вмешательства и/или процедуры"
    },
    {
      "code": "ДРУГОЕ",
      "caption": "Другое"
    }
  ]
}
```

### Пример java

```java
public class GetTm66ConclusionTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> tm66ConclusionTypes = client.getTm66ConclusionTypes();
        Directories.Tm66ConclusionType tm66ConclusionType = tm66ConclusionTypes.get(0);

        String id = tm66ConclusionType.getId();
        String caption = tm66ConclusionType.getCaption();
    }
}

```