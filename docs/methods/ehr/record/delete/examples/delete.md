### Удаление записи из указанного заболевания

### ![POST](../../../../../../img/post.png) [/ehr/record/delete](../index.md)

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/delete HTTP/1.1`

```json
{
    "record":{
        "id":"#881:11797",
        "patient_id":"#65:10693",
        "ehr_id": "#64:163"
    }
}
```

**Response**
```json
{
  "result": [
  ]
}
```
