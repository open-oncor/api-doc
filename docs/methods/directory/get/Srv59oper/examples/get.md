[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/Srv59oper](../index.md)

### HTTP примеры

**Request**  GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/Srv59Oper HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "code":"SRV_1_1_1",
            "caption":"Первичной опухоли, в том числе с удалением регионарных лимфатических узлов",
            "group":1,
            "index":1
        },
        {
            "code":"SRV_1_1_2",
            "caption":"Метастазов",
            "group":1,
            "index":2
        },
        {
            "code":"SRV_1_1_3",
            "caption":"Симптоматическое",
            "group":1,
            "index":3
        },
        {
            "code":"SRV_1_1_4",
            "caption":"Выполнено хирургическое стадирование",
            "group":1,
            "index":4
        },
        {
            "code":"SRV_1_1_5",
            "caption":"Регионарных лимфатических узлов без первичной опухоли",
            "group":1,
            "index":5
        },
        {
            "code":"SRV_1_1_6",
            "caption":"Циторедуктивное",
            "group":1,
            "index":6
        },
        {
            "code":"SRV_1_1_7",
            "caption":"Паллиативное",
            "group":1,
            "index":7
        },
        {
            "code":"SRV_1_1_8",
            "caption":"Операции с реконструктивно-пластическим компонентом, в т.ч. установка импланта",
            "group":1,
            "index":8
        }
    ]
}
```

**[Java пример](getJava.md)**