[Работа с пациентами](../../index.md)
=====================================

### ![POST](../../../../img/post.png) [/patient/search](../../search/index.md)

### Примеры

**Request**

POST `http://tempurl.com/patient/search HTTP/1.1`
```json
{
    "patient_query":{
        "first_name":"Татьяна",
        "middle_name":"Ивановна",
        "last_name":"Шмакова",
        "birth_day":"1952-06-14"
    }
}
```

**Request `200`**
```json
{
    "patient_query":{
        "first_name":"Татьяна",
        "middle_name":"Ивановна",
        "last_name":"Шмакова",
        "birth_day":"1952-06-14"
    }
}
```

**Request `422`**
```json
{
    "error":{
        "name":"com.siams.med.api.InvalidArgumentsException",
        "message":"Invalid patient name",
        "uuid":"d2eaae0f-274b-4254-8b69-163c2c3a6143"
    }
}
```

**[Примеры кода](searchCode.md)**