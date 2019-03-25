## Справочник групп крови

### ![GET](../../../../img/get.png) /directory/get/BloodType
* **URL Parametr: Добавить URL parameter**
* **Response: [[BloodType](../../../../types/types.md#com.siams.med.api.BloodType)]**

В ответе передаётся массив записей из справочника

### Пример http
**Request:** GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/BloodType HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"I_N",
            "caption":"0(I)Rh-"
        },
        {
            "id":"I_P",
            "caption":"0(I)Rh+"
        },
        {
            "id":"II_N",
            "caption":"A(II)Rh-"
        },
        {
            "id":"II_P",
            "caption":"A(II)Rh+"
        },
        {
            "id":"III_N",
            "caption":"B(III)Rh-"
        },
        {
            "id":"III_P",
            "caption":"B(III)Rh+"
        },
        {
            "id":"IV_N",
            "caption":"AB(IV)Rh-"
        },
        {
            "id":"IV_P",
            "caption":"AB(IV)Rh+"
        }
    ]
}
```

### Пример java

```java
public class GetBloodTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.BloodType> bloodTypes = client.getBloodTypes();
        Directories.BloodType bloodType = bloodTypes.get(0);

        String id = bloodType.getId();
        String caption = bloodType.getCaption();
    }
}
```
