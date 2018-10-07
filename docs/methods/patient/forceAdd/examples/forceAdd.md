[Работа с пациентами](../index.md)
==================================

### ![GET](../../../../img/get.png) [/patient/forceAdd](../index.md)

**Request**

POST `http://tempurl.com/patient/forceAdd HTTP/1.1`
```json
{
    "patient":{
          "first_name":"Сергей",
          "middle_name":"Сергеевич",
          "last_name":"Сергеев",
          "birth_day":"1977-01-0",
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

**[Примеры кода](forceAddCode.md)**