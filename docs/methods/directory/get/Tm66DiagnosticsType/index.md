## Справочник Тип диагностики ДЭЗО

### ![GET](../../../../img/get.png) /directory/get/Tm66DiagnosticsType
* **Response: [[Tm66DiagnosticsType](../../../../types/types.md#com.siams.med.api.Tm66DiagnosticsType)]**

### Пример http


**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/Tm66DiagnosticsType HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**

```json

{
  "result": [
    {
      "code": "РГ_ГРУДНОЙ_КЛЕТКИ",
      "caption": "Рентгенография органов грудной клетки"
    },
    {
      "code": "РГ_ЖЕЛУДКА_ПИЩЕВОДА",
      "caption": "Рентгенография желудка/пищевода"
    },
    {
      "code": "КТ_ГОЛОВЫ",
      "caption": "Компьютерная томография головы"
    },
    {
      "code": "КТ_ШЕИ",
      "caption": "Компьютерная томография шеи"
    },
    {
      "code": "КТ_ГРУДНОЙ_КЛЕТКИ",
      "caption": "Компьютерная томография грудной клетки"
    },
    {
      "code": "КТ_БРЮШНОЙ_ПОЛОСТИ",
      "caption": "Компьютерная томография брюшной полости"
    },
    {
      "code": "КТ_ТАЗА",
      "caption": "Компьютерная томография таза"
    },
    {
      "code": "КТ_КОСТЕЙ_И_СУСТАВОВ",
      "caption": "Компьютерная томография костей и суставов"
    },
    {
      "code": "КТ_СЕРДЦА",
      "caption": "Компьютерная томография сердца"
    },
    {
      "code": "МРТ_ГОЛОВЫ",
      "caption": "Магниторезонансная томография головы"
    },
    {
      "code": "МРТ_ШЕИ",
      "caption": "Магниторезонансная томография шеи"
    },
    {
      "code": "МРТ_ГРУДНОЙ_КЛЕТКИ",
      "caption": "Магниторезонансная томография грудной клетки"
    },
    {
      "code": "МРТ_БРЮШНОЙ_ПОЛОСТИ",
      "caption": "Магниторезонансная томография брюшной полости"
    },
    {
      "code": "МРТ_ТАЗА",
      "caption": "Магниторезонансная томография таза"
    },
    {
      "code": "МРТ_КОСТЕЙ_И_СУСТАВОВ",
      "caption": "Магниторезонансная томография костей и суставов"
    },
    {
      "code": "МРТ_СЕРДЦА",
      "caption": "Магниторезонансная томография сердца"
    },
    {
      "code": "МРТ_СОСУДОВ",
      "caption": "Магниторезонансная томография сосудов"
    },
    {
      "code": "УЗИ_БРЮШНОЙ_ПОЛОСТИ",
      "caption": "Ультразвуковое исследование брюшной полости"
    },
    {
      "code": "УЗИ_МАЛОГО_ТАЗА",
      "caption": "Ультразвуковое исследование малого таза"
    },
    {
      "code": "УЗИ_МОЛОЧНЫХ_ЖЕЛЕЗ",
      "caption": "Ультразвуковое исследование молочных желез"
    }
  ]
}
```

### Пример java

```java
public class GetTm66DiagnosticsTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> tm66DiagnosticsTypes = client.getTm66DiagnosticsTypes();
        Directories.Tm66DiagnosticsType tm66DiagnosticsType = tm66DiagnosticsTypes.get(0);

        String id = tm66DiagnosticsType.getId();
        String caption = tm66DiagnosticsType.getCaption();
    }
}

```