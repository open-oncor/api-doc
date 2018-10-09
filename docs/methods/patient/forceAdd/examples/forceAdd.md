Добавление пациента без анализа 'двойников' (http)
=

### ![GET](../../../../img/get.png) [/patient/forceAdd](../index.md)

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/forceAdd HTTP/1.1`
```json
{
    "patient":{
          "first_name":"Сергей",
          "middle_name":"Сергеевич",
          "last_name":"Сергеев",
          "birth_day":"1977-01-0"
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#71:32905",
            "first_name":"Сергей",
            "middle_name":"Сергеевич",
            "last_name":"Сергеев",
            "birth_day":"1977-01-01",
            "code":"",
            "ehr_count":0,
            "company_name":"",
            "snils":""
        }
    ]
}
```

