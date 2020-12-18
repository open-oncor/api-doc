## Справочник Причины отказа проведения ДЭЗО

### ![GET](../../../../img/get.png) /directory/get/Tm66OrderRejectReason
* **Response: [[Tm66OrderRejectReason](../../../../types/types.md#com.siams.med.api.Tm66OrderRejectReason)]**

### Пример http


**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/Tm66OrderRejectReason HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**
```json

{
  "result": [
    {
      "id": "1",
      "code": "ДАННЫЕ_ПАЦИЕНТА",
      "caption": "Недостаточно данных о пациенте"
    },
    {
      "id": "2",
      "code": "КАЧЕСТВО_СНИМКА",
      "caption": "Снимок выполнен некачественно"
    },
    {
      "id": "3",
      "code": "ОБЛАСТЬ_СНИМКА",
      "caption": "Не совпадают локализации ДЭЗО и область снимка"
    },
    {
      "id": "4",
      "code": "НЕВОЗМОЖНО_АССОЦИИРОВАТЬ",
      "caption": "Невозможно ассоциировать снимок и ДЭЗО"
    }
  ]
}
```

### Пример java

```java
public class GetTm66OrderRejectReasons {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> tm66OrderRejectReasons = client.getTm66OrderRejectReasons();
        Directories.Tm66OrderRejectReason tm66OrderRejectReason = tm66OrderRejectReasons.get(0);

        String id = tm66OrderRejectReason.getId();
        String caption = tm66OrderRejectReason.getCaption();
    }
}

```