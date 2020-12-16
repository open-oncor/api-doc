## Список медицинских организаций региона

### ![GET](../../../../img/get.png) /medOrg/getList
* **Response:** [[MedOrg](../../../../types/types.md#com.siams.med.api.MedOrg)]

Возвращает список медицинских организаций [MedOrg](../../../../types/types.md#com.siams.med.api.MedOrg) из системы oncor отсутствующих в реестре 
“Регистр медицинских организаций Российской Федерации".



### Пример http
**Request**  

GET `https://demo.onco-reg.ru/api/1.0/json/medOrg/getList HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

**Response**

```json
{
    "result":[
        {
            "id":"#985:0",
            "unq":"1.2.643.2.75.1.100.1.66.661609",
            "name_full":"Муниципальное унитарное предприятие \" Эстедент \"",
            "name_short":"Муниципальное унитар",
            "kpp":"",
            "ogrn":"0",
            "inn":"",
            "okato":"",
            "post_index":"",
            "address":"г.Талица",
            "med_terr":{
                "id":"#33:8",
                "unq":"1.2.643.2.75.1.100.2.66.660401",
                "federal_code":"66",
                "code":"401",
                "name":"Талицкий гор. округ",
                "okato":"65249000000"
            },
            "org_unit_id":"#993:0"
        },
        {
            "id":"#985:1",
            "unq":"1.2.643.2.75.1.100.1.66.660044",
            "name_full":"Государственное учреждение здравоохранения Свердл. обл.\"Специализированный дом ребенка №9\"",
            "name_short":"ГУЗ СО СД Реб.№ 9",
            "kpp":"",
            "ogrn":"1036601476691",
            "inn":"",
            "okato":"",
            "post_index":"",
            "address":"Свердловская обл., г. Первоуральск, ул. Комсомольская, 9\"А\"",
            "med_terr":{
                "id":"#35:1",
                "unq":"1.2.643.2.75.1.100.2.66.660901",
                "federal_code":"66",
                "code":"901",
                "name":"Гор. округ Первоуральск",
                "okato":"65480000000"
            },
            "org_unit_id":"#993:1"
        },
        ...
    ]
}
```