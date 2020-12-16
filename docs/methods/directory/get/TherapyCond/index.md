## Справочник условий проведения лечения

### ![GET](../../../../img/get.png) /directory/get/TherapyCond
* **Response:** [[TherapyCond](../../../../types/types.md#com.siams.med.api.TherapyCond)]

В ответе передаётся массив записей из справочника [TherapyCond](../../../../types/types.md#com.siams.med.api.TherapyCond).


### Пример http

**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/TherapyCond HTTP/1.1
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}
Content-Type: application/json`

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