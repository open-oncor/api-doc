## Справочник стадий

### ![GET](../../../../img/get.png) /directory/get/DzStage
* **Response: [[DzStage](../../../../types/types.md#com.siams.med.api.DzStage)]**

В ответе передаётся массив записей из справочника [DzStage](../../../../types/types.md#com.siams.med.api.DzStage).

### Пример http
**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/DzStage HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**


```json
{
    "result": [
        {
            "code": "NONE",
            "caption": ""
        },
        {
            "id": "4",
            "code": "I",
            "caption": "I"
        },
        {
            "id": "1",
            "code": "I_A",
            "caption": "Ia"
        },
        {
            "id": "2",
            "code": "I_B",
            "caption": "Ib"
        },
        {
            "id": "3",
            "code": "I_C",
            "caption": "Ic"
        },
        {
            "id": "8",
            "code": "II",
            "caption": "II"
        },
        {
            "id": "5",
            "code": "II_A",
            "caption": "IIa"
        },
        {
            "id": "6",
            "code": "II_B",
            "caption": "IIb"
        },
        {
            "id": "7",
            "code": "II_C",
            "caption": "IIc"
        },
        {
            "id": "12",
            "code": "III",
            "caption": "III"
        },
        {
            "id": "9",
            "code": "III_A",
            "caption": "IIIa"
        },
        {
            "id": "10",
            "code": "III_B",
            "caption": "IIIb"
        },
        {
            "id": "11",
            "code": "III_C",
            "caption": "IIIc"
        },
        {
            "id": "16",
            "code": "IV",
            "caption": "IV"
        },
        {
            "id": "13",
            "code": "IV_A",
            "caption": "IVa"
        },
        {
            "id": "14",
            "code": "IV_B",
            "caption": "IVb"
        },
        {
            "id": "15",
            "code": "IV_C",
            "caption": "IVc"
        },
        {
            "id": "17",
            "code": "IN_SITU",
            "caption": "in situ"
        },
        {
            "id": "18",
            "code": "NA",
            "caption": "неприменимо"
        }
    ]
}
```
