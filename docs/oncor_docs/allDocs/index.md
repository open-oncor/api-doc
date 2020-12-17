## Поиск среди всех документов


### Пример http

**Параметры запроса:**  
q - искомый текст или код МКБ10  
offset (optional) - смещение, по умолчанию 0  
limit (optional) - количество, по умолчанию 200  

**Request:**

GET `https://demo.onco-reg.ru/docs/api?q=кожа`

**Response 200**

```json
{
  "result": {
    "total": 58,
    "offset": 0,
    "documents": [
      {
        "description": "Критерии качества специализированной медицинской помощи взрослым при злокачественной меланоме и других злокачественных новообразованиях кожи (код по МКБ-10: C43)",
        "type": "Критерии качества",
        "link": "http://demo.oncor.pro/docs/oncor-docs/regulations/66/2381-p/qc(C43).pdf"
      },
      {
        "description": "Критерии качества специализированной медицинской помощи взрослым при других злокачественных новообразованиях кожи (код по МКБ-10: C44)",
        "type": "Критерии качества",
        "link": "http://demo.oncor.pro/docs/oncor-docs/regulations/66/2381-p/qc(C44).pdf"
      },
      {
        "description": "#Критерии качества специализированной медицинской помощи взрослым при злокачественном новообразовании кожи (код по МКБ-10: С44)",
        "type": "Критерии качества",
        "link": "http://demo.oncor.pro/docs/oncor-docs/regulations/25/35-p/%D0%A144.pdf"
      },
     ...
   ]
  }
}
```

**Response 422**
```json
{
  "error": {
    "class": "IndexOutOfBoundsException",
    "message": "fromIndex = -10"
  }
}
```