### Удаление записи указанного пациента

### ![POST](../../../../../../img/post.png) [/patient/record/delete](../index.md)

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/delete HTTP/1.1`

```json
{
    "record":{
        "id":"#881:11797",
        "patient_id":"#65:10693"
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
