## Справочник половой принадлежности

### ![GET](../../../../img/get.png) /directory/get/Gender

* **Response: [[DrPrsG](../../../../types/types.md#com.siams.med.api.DrPrsG)]**

В ответе передаётся массив записей из справочника [DrPrsG](../../../../types/types.md#com.siams.med.api.DrPrsG).

### Пример http
**Request** 

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/DrPrsG HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "orid":"#721:0",
            "id":"1",
            "caption":"М"
        },
        {
            "orid":"#722:0",
            "id":"",
            "caption":"Пол"
        },
        {
            "orid":"#723:0",
            "id":"2",
            "caption":"Ж"
        },
        {
            "orid":"#724:0",
            "id":"3",
            "caption":"не определено"
        }
    ]
}
```



### Пример java

```java
public class GetPrsG {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.DrPrsG> genders = client.getGenders();
        Directories.DrPrsG drPrsG = genders.get(0);

        String id = drPrsG.getId();
        String caption = drPrsG.getCaption();
    }
}
```