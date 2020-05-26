## Добавление пациента

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types/types.md#com.siams.med.api.Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response :** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#com.siams.med.api.ErrorResult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/patient/add HTTP/1.1`

```json
{
    "patient":{
        "first_name":"Иван",
        "middle_name":"Иванович",
        "last_name":"Иванов",
        "birth_day":"1901-01-01",
        "gender":{
            "id":"1"
        },
        "phones":"+7 911",
        "address": {
          "address": "г. Верхняя Пышма, ул. Серова, д.34, кв. 56",
          "med_terr": {
            "id": "#35:4",
            "name": "Гор. округ Верхняя Пышма"
          }
        }

    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#65:33650",
            "first_name":"Иван",
            "middle_name":"Иванович",
            "last_name":"Иванов",
            "birth_day":"1901-01-01",
            "gender":{
                "orid":"#721:0",
                "id":"1",
                "caption":"М"
            },
            "code":"ИИИ010101М",
            "ehr_count":0,
            "company_name":"",
            "snils":"",
            "phones":"+7 911",
            "address": {
              "address": "г. Верхняя Пышма, ул. Серова, д.34, кв. 56",
              "med_terr": {
                  "id": "#35:4",
                  "unq": "1.2.643.2.75.1.100.2.66.661102",
                  "federal_code": "66",
                  "code": "1102",
                  "name": "Гор. округ Верхняя Пышма",
                  "okato": "65420000000"
              }
            }

        }
    ]
}
```

**Response `422`**

```json
{
    "error":{
        "name":"InvalidArgumentsException",
        "message":"Invalid patient name",
        "uuid":"16bfee9a-2616-4a58-85c2-9ba4ac782cf4"
    }
}
```


### Пример java

```java
class AddPatient {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();

        client.addPatient(Patients.Patient.newBuilder()
                .setFirstName("Иван")
                .setMiddleName("Иванович")
                .setLastName("Иванов")
                .setBirthDay("1901-01-01")
                .setPhones("+7 911")
                .setGender(Directories.DrPrsG.newBuilder()
                        .setId("1")
                        .build())
                .build());

    }
}
```
