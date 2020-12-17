## Поиск клинических рекомендаций


### Пример http

**Параметры запроса:**  

q - искомый текст или код МКБ10  
type  (optional) - Тип документа  
offset (optional) - смещение, по умолчанию 0  
limit (optional) - количество, по умолчанию 200  

**Типы документов:**  

clinical - "Клинические рекомендации"  
logic - "Алгоритм"  
quality - "Критерии качества"  
chemotherapy - "Схема химиотерапии"  
else - "Иные"  

**Request:**

GET `https://demo.onco-reg.ru/docs/api?q=C53&type=quality&offset=0&limit=10`

**Response 200**

OK  
OUT_OF_RANGE - page и size за пределами списка найденных документов  
NO_RESULTS - ничего не найдено  

```json
{
  "result": {
    "total": 2,
    "offset": 0,
    "documents": [
      {
        "description": "Критерии качества специализированной медицинской помощи взрослым при злокачественном новообразовании шейки матки (код по МКБ-10: C53)",
        "type": "Критерии качества",
        "link": "http://demo.oncor.pro/docs/oncor-docs/regulations/66/2381-p/qc(C53).pdf"
      },
      {
        "description": "#Критерии качества специализированной медицинской помощи взрослым при злокачественном новообразовании вульвы, влагалища, шейки матки (код по МКБ-10: С51-С53)",
        "type": "Критерии качества",
        "link": "http://demo.oncor.pro/docs/oncor-docs/regulations/25/35-p/%D0%A151_53.pdf"
      }
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