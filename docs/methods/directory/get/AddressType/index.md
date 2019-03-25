## Справочник типов адресов

### ![GET](../../../../img/get.png) /directory/get/AddressType
* **Response: [[AddressType](../../../../types/types.md#com.siams.med.api.AddressType)]**

В ответе передаётся массив записей из справочника [AddressType](../../../../types/types.md#com.siams.med.api.AddressType).


### Пример http


GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/AddressType HTTP/1.1`

**Response**
```json



{
    "result":[
        {
            "id":"HP",
            "caption":"Адрес регистрации"
        },
        {
            "id":"H",
            "caption":"Адрес фактического проживания"
        },
        {
            "id":"NULL",
            "caption":"Адрес места рождения"
        },
        {
            "id":"WP",
            "caption":"Служебный адрес"
        },
        {
            "id":"DIR",
            "caption":"Прямой почтовый или телекоммуникационный адрес рабочего места"
        },
        {
            "id":"PUB",
            "caption":"Общий почтовый или телекоммуникационный адрес рабочего места"
        },
        {
            "id":"BAD",
            "caption":"Неправильный адрес"
        },
        {
            "id":"TMP",
            "caption":"Временный адрес"
        },
        {
            "id":"PST",
            "caption":"Адрес для писем"
        }
    ]
}
```

### Пример java

```java
public class GetAddressTypes {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.AddressType> addressTypes = client.getAddressTypes();
        Directories.AddressType addressType = addressTypes.get(0);

        String id = addressType.getId();
        String caption = addressType.getCaption();
    }
}

```