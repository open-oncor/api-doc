## Справочник типов отдаленных метастаз

### ![GET](../../../../img/get.png) /directory/get/LocMetType
* **Response:** [[LocMetType](../../../../types/types.md#com.siams.med.api.LocMetType)]

В ответе передаётся массив записей из справочника [LocMetType](../../../../types/types.md#com.siams.med.api.LocMetType).



### Пример http

**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/LocMetType HTTP/1.1`  
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}  
Content-Type: application/json

**Response**
```json
{
    "result":[
        {
            "caption":"неизвестно",
            "code":"UNKNOWN"
        },
        {
            "caption":"отдален. лимф. узлы",
            "code":"RLN"
        },
        {
            "caption":"кости",
            "code":"BONES"
        },
        {
            "caption":"печень",
            "code":"LIVER"
        },
        {
            "caption":"легкие и/или плевра",
            "code":"LUNG"
        },
        {
            "caption":"головной мозг",
            "code":"BRAIN"
        },
        {
            "caption":"кожа",
            "code":"SKIN"
        },
        {
            "caption":"почки",
            "code":"KIDNEY"
        },
        {
            "caption":"яичники",
            "code":"OVARY"
        },
        {
            "caption":"брюшина",
            "code":"PERITONEUM"
        },
        {
            "caption":"костный мозг",
            "code":"BONE_MARROW"
        },
        {
            "caption":"другие органы",
            "code":"OTHER_ORGANS"
        },
        {
            "caption":"множественные",
            "code":"PLURAL"
        }
    ]
}
```

### Пример java

```java
public class GetLocMetTypeDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.LocMetType> locMetTypeDirectory = client.getLocMetTypeDirectory();
        Directories.LocMetType locMetType = locMetTypeDirectory.get(0);

        String caption = locMetType.getCaption();
        Directories.LocMet.Code code = locMetType.getCode();
    }
}
```