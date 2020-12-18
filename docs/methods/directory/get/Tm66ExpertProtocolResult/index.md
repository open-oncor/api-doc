## Справочник типа значимости замечаний эксперта к к первичному протоколу исследования

### ![GET](../../../../img/get.png) /directory/get/Tm66ExpertProtocolResult
* **Response: [[Tm66ExpertProtocolResult](../../../../types/types.md#com.siams.med.api.Tm66ExpertProtocolResult)]**

### Пример http

**Request**

 GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/Tm66ExpertProtocolResult`  
 `X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
 `Content-Type: application/json`

**Response**
```json
{
  "result": [
    {
      "code": "НАРУШЕНИЙ_НЕТ",
      "caption": "Нарушений нет"
    },
    {
      "code": "НЕЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
      "caption": "Выявлены незначительные нарушения, не влияющие на сформированное заключение"
    },
    {
      "code": "ЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
      "caption": "Выявленные значительные нарушения, кардинальным образом меняющие сформированное заключение"
    }
  ]
}
```