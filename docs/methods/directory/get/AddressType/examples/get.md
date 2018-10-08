[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/Gender](../index.md)

### HTTP примеры

**Response**

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/AddressType HTTP/1.1`
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

**[Java пример](getJava.md)**