## Справочник Цель ДЭЗО

### ![GET](../../../../img/get.png) /directory/get/Tm66OrderPurpose
* **Response: [[Tm66OrderPurpose](../../../../types/types.md#com.siams.med.api.Tm66OrderPurpose)]**

### Пример http


**Request** 

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/Tm66OrderPurpose HTTP/1.1`

**Response**

```json
{
  "result": [
    {
      "id": "1",
      "code": "ПОДТВЕРЖДЕНИЕ_ДИАГНОЗА",
      "caption": "Определение (подтверждение) диагноза"
    },
    {
      "id": "2",
      "code": "ПОДТВЕРЖДЕНИЕ_ТАКТИКИ",
      "caption": "Определение (подтверждение) тактики лечения"
    },
    {
      "id": "3",
      "code": "СОГЛАСОВАНИЕ_ГОСПИТАЛИЗАЦИИ",
      "caption": "Согласование условий и срока госпитализации в ФГБУ"
    },
    {
      "id": "4",
      "code": "НЕОБХОДИМОСТЬ_ВМЕШАТЕЛЬСТВА",
      "caption": "Необходимость выполнение нового и/или редкого вида оперативного вмешательства, процедуры и т.д."
    },
    {
      "id": "5",
      "code": "ФОРМИРОВАНИЕ_ЭКСПЕРТНОГО_МНЕНИЯ",
      "caption": "Формирование экспертного мнения по результатам диагностических исследований (МСКТ, МРТ, ПЭТ-КТ и т.п.)"
    },
    {
      "id": "6",
      "code": "РАЗБОР_КЛИНИЧЕСКИХ_СЛУЧАЕВ",
      "caption": "Разбор клинических случаев"
    },
    {
      "id": "7",
      "code": "ДРУГОЕ",
      "caption": "Другое"
    }
  ]
}
```

### Пример java

```java
public class GetTm66OrderPurposes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> tm66OrderPurposes = client.getTm66OrderPurposes();
        Directories.Tm66OrderPurpose tm66OrderPurpose = tm66OrderPurposes.get(0);

        String id = tm66OrderPurpose.getId();
        String caption = tm66OrderPurpose.getCaption();
    }
}

```