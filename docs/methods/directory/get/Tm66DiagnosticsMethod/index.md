## Справочник Типа инструментальной диагностики в первичном протоколе исследования

### ![GET](../../../../img/get.png) /directory/get/Tm66DiagnosticsMethod
* **Response: [[Tm66DiagnosticsMethod](../../../../types/types.md#com.siams.med.api.Tm66DiagnosticsMethod)]**

Справочник используется в первичном протоколе исследования [заявки на ДЭЗО](../../../../methods/search/get/RecordsPage/index.md)

### Пример http

**Request** 

GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/Tm66DiagnosticsMethod HTTP/1.1`

**Response**

```json
{
  "result": [
    {
      "code": "РГ",
      "caption": "Рентгенография"
    },
    {
      "code": "КТ",
      "caption": "Компьютерная томография"
    },
    {
      "code": "МРТ",
      "caption": "Магниторезонансная томография"
    },
    {
      "code": "УЗИ",
      "caption": "Ультразвуковое исследование"
    }
  ]
}
```