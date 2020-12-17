## Поиск клинических рекомендаций


### Пример http

**Параметры запроса:**  

q - искомый текст или код МКБ10  
type  (optional) - Тип документа   
offset (optional) - смещение, по умолчанию 0  
limit (optional) - количество, по умолчанию 200  

**Request:**

GET `https://demo.onco-reg.ru/docs/api?q=кожа&type=clinical&offset=0&limit=10`

**Response 200**

```json
{
  "result": {
    "total": 42,
    "offset": 0,
    "documents": [
      {
        "description": "Рак гортани МКБ 10: C32 Возрастная категория: взрослые Год утверждения: 2017",
        "type": "Клинические рекомендации",
        "link": "http://demo.oncor.pro/docs/oncor-docs/clinical-guidelines/aor2020/gs/rak_gortani.pdf"
      },
      {
        "description": "Злокачественные опухоли костей МКБ 10: C40/C41 Возрастная категория: взрослые Год утверждения: 2017",
        "type": "Клинические рекомендации",
        "link": "http://demo.oncor.pro/docs/oncor-docs/clinical-guidelines/aor2020/bone/zlokachestvennye_opukholi_kostey.pdf"
      },
      {
        "description": "Саркомы мягких тканей МКБ 10: C49 Возрастная категория: взрослые Год утверждения: 2017",
        "type": "Клинические рекомендации",
        "link": "http://demo.oncor.pro/docs/oncor-docs/clinical-guidelines/aor2020/bone/sarkomy_myagkikh_tkaney.pdf"
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