## Получение медицинской записи пациента по ключу

### ![GET](../../../img/get.png) /rc/get`?id={id}`
* **URL parameter:** [id](../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../types/types.md#com.siams.med.api.Rc)]

### Пример http

**Request:** 

GET `https://demo.onco-reg.ru/api/1.0/json/rc/get?id=1577:16819 HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

**Response**

```json
{
    "result":[
        {
            "id":"#1577:16819",
            "class_name":"RcDoc",
            "patient_id":"#70:29080",
            "ehr_id":"#1054:29080",
            "published":{
                "user_id":"#961:97",
                "time":"2018-08-08 08:12:29"
            },
            "org_unit_id":"#999:28",
            "summary":"Биохимическое исследование крови",
            "time_rc":"2018-02-09 00:00:00",
            "rc_doc":{
                "category":"EXAMPLE",
                "html":"<b>Example</b>"
            }
        }
    ]
}
```
