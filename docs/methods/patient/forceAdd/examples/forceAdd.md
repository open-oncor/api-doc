[Работа с пациентами](../index.md)
==================================

### ![GET](../../../../img/get.png) [/patient/forceAdd](../index.md)

**Request**

POST `http://tempurl.com/patient/forceAdd HTTP/1.1`
```json
{
    "patient":{
    }
}
```

**Response**
```json
{
    "result":[
        {
            "id":"#71:32905",
            "first_name":"",
            "middle_name":"",
            "last_name":"",
            "birth_day":"",
            "code":"",
            "ehr_count":0,
            "company_name":"",
            "snils":""
        }
    ]
}
```