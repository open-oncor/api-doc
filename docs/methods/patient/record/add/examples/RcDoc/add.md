### Добавление медицинской записи пациенту (RcDoc)

### ![POST](../../../../../../img/post.png) [/patient/record/add](../../index.md)

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/add HTTP/1.1`
```json
{
  "record": {
    "patient_id": "#69:14084",
    "summary": "Протокол химиотерапии (mo1)",
    "rc_doc": {
      "html": "<body><h1>Протокол химиотерапии</h1>Данные протокола находятся здесь</body>",
      "category": "лечение"
    },
    "time_rc": "2018-06-01"
  }
}
```

**Response**
```json
{
  "result": [
    {
      "id": "#1580:36890",
      "class_name": "RcDoc",
      "patient_id": "#69:14084",
      "ehr_id": "#1053:14084",
      "published": {
        "user_id": "#961:97",
        "time": "2018-12-28 13:24:32"
      },
      "org_unit_id": "#999:28",
      "summary": ".Протокол химиотерапии (mo1)",
      "time_rc": "2018-06-01 00:00:00",
      "rc_doc": {
        "category": "лечение",
        "html": "<body><h1>Протокол химиотерапии</h1>Данные протокола находятся здесь</body>"
      }
    }
  ]
}
```
