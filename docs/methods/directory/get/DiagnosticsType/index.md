## Справочник диагностических исследований

### ![GET](../../../../img/get.png) /directory/get/DiagnosticsType

* **Response: [[DiagnosticsType](../../../../types/types.md#com.siams.med.api.DiagnosticsType)]**

В ответе передаётся массив записей из справочника [DiagnosticsType](../../../../types/types.md#com.siams.med.api.DiagnosticsType).

### Пример http
**Request:** 

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/DiagnosticsType HTTP/1.1`

**Response**

```json
{
    "result": [
        {
            "code": "OAM",
            "caption": "ОАМ"
        },
        {
            "code": "OAK",
            "caption": "ОАК"
        },
        {
            "code": "BAB",
            "caption": "биохимия крови"
        },
        {
            "code": "X_RAY_CHEST",
            "caption": "рентгенография грудной клетки"
        },
        {
            "code": "X_RAY_GORT",
            "caption": "рентгенография гортани"
        },
        {
            "code": "FLS",
            "caption": "ФЛС"
        },
        {
            "code": "FBS",
            "caption": "ФБС"
        },
        {
            "code": "US_ABDOMINAL",
            "caption": "УЗИ брюшной полости"
        },
        {
            "code": "US_PELVIC",
            "caption": "УЗИ малого таза"
        },
        {
            "code": "MRT_PELVIC",
            "caption": "МРТ малого таза"
        },
        {
            "code": "KT_CHEST",
            "caption": "КТ грудной клетки"
        },
        {
            "code": "KT_ABDOMINAL",
            "caption": "КТ брюшной полости"
        },
        {
            "code": "MRT_ABDOMINAL",
            "caption": "МРТ брюшной полости"
        },
        {
            "code": "MRT_CNS",
            "caption": "МРТ ЦНС"
        },
        {
            "code": "KT_H_N",
            "caption": "КТ головы и шеи"
        },
        {
            "code": "US_MAM_GLAND",
            "caption": "УЗИ молочных желез"
        },
        {
            "code": "MAMMO",
            "caption": "маммография"
        },
        {
            "code": "FGDS",
            "caption": "ФГДС"
        },
        {
            "code": "X_RAY_STOMACH",
            "caption": "рентгенография желудка/пищевода"
        },
        {
            "code": "FKS",
            "caption": "ФКС"
        },
        {
            "code": "IRRIGOSCOPY",
            "caption": "ирригоскопия"
        },
        {
            "code": "GINEK_CITOLOG",
            "caption": "гинекологический осмотр"
        },
        {
            "code": "HISTOLOGY",
            "caption": "гистология"
        },
        {
            "code": "CYTOLOGY",
            "caption": "цитология"
        },
        {
            "code": "PSA",
            "caption": "ПСА"
        },
        {
            "code": "TRUZI",
            "caption": "ТРУЗИ"
        },
        {
            "code": "CISTOSCOP",
            "caption": "цистоскопия"
        }
    ]
}
```


### Пример java
Добавить