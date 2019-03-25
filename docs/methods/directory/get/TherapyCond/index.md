## Справочник условий проведения лечения

### ![GET](../../../../img/get.png) /directory/get/TherapyCond
* **Response:** [[TherapyCond](../../../../types/types.md#com.siams.med.api.TherapyCond)]

В ответе передаётся массив записей из справочника [TherapyCond](../../../../types/types.md#com.siams.med.api.TherapyCond).


### Пример http

**Request** 

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/TherapyCond HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "code":"NONE",
            "caption":""
        },
        {
            "id":"1",
            "code":"AMB",
            "caption":"амбулаторно"
        },
        {
            "id":"2",
            "code":"HOSP",
            "caption":"стационарно"
        }
    ]
}
```

### Пример java

```java
public class GetTherapyCondDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.TherapyCond> therapyCondDirectory = client.getTherapyCondDirectory();
        Directories.TherapyCond therapyCond = therapyCondDirectory.get(0);

        String id = therapyCond.getId();
        String caption = therapyCond.getCaption();
    }
}

```