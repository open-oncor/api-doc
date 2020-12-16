## Справочник типов адресов

### ![GET](../../../../img/get.png) /directory/get/AddressType
* **Response: [[AddressType](../../../../types/types.md#com.siams.med.api.AddressType)]**

В ответе передаётся массив записей из справочника [AddressType](../../../../types/types.md#com.siams.med.api.AddressType).


### Пример http


**Request** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/AddressType HTTP/1.1
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}
Content-Type: application/json`

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
