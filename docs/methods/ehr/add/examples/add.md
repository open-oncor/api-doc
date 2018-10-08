[Работа с заболеваниями пациента](../../index.md)
=====================================================

### ![POST](../../../../img/post.png) [/ehr/add](../index.md)

### Примеры

**Request**

POST `http://tempurl.com/ehr/add HTTP/1.1`
```json
{
    "ehr":{
        "patient_id":"#66:33481"
    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#873:36386",
            "patient_id":"#66:33481",
            "summary":""
        }
    ]
}
```

**Response `422`**
```json
{
    "error":{
        "name":"com.siams.med.api.PatientNotFoundException",
        "message":"Patient \"\" not found",
        "uuid":"9b2ef941-b81d-43e3-8e87-e8b0dad6e6e2"
    }
}
```