## Добавление пациента без анализа 'двойников'

### ![POST](../../../img/post.png) /patient/forceAdd
* **Request:** [Patient](../../../types/types.md#com.siams.med.api.Patient) 
* **Response:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]

### Пример http 

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

### Пример java

```java
class AddPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        client.forceAddPatient(Patients.Patient.newBuilder()
                .setFirstName("Сергеев")
                .setMiddleName("Сергей")
                .setLastName("Сергеевич")
                .setBirthDay("1977-01-01")
                .build());
    }
}
```
