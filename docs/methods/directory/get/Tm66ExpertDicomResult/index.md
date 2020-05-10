## Справочник типа значимости замечаний эксперта к DICOM 

### ![GET](../../../../img/get.png) /directory/get/Tm66ExpertDicomResult
* **Response: [[Tm66ExpertDicomResult](../../../../types/types.md#com.siams.med.api.Tm66ExpertDicomResult)]**

### Пример http

**Request**

   GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/Tm66ExpertDicomResult`

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
      "caption": "Выявлены незначительные нарушения, обусловленные оборудованием, на котором проводилось исследование"
    },
    {
      "code": "ЗНАЧИТЕЛЬНЫЕ_НАРУШЕНИЯ",
      "caption": "Выявленные значительные нарушения, не позволяющие сделать достоверные заключения"
    }
  ]
}
```