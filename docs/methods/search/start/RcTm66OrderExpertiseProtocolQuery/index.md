# Поиск документов "Экспертиза качества первичного протокола исследования"

### Пример http
1. Стартуем поиск документов "Экспертиза качества первичного протокола исследования"
**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/search/start/RcTm66OrderExpertiseProtocolQuery HTTP/1.1`    
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
  "query": {
    "from_date": "2020-01-01"
  }
}
```
**Response**
```json
{
  "result": [
    {
      "id": "68f9bb9d-ae5f-457f-9299-5809757bccbc"
    }
  ]
}
```
2. Запрос страницы с результатами
**Request**  
```json
{
  "page":{
    "job":{
      "id":"fac8d822-a14f-448b-90e7-07a5ec6495e0"
    },
    "offset":0,
    "size":3
  }
}
```
**Response**
```json
{
  "result": [
    {
      "page": {
        "job": {
          "id": "68f9bb9d-ae5f-457f-9299-5809757bccbc",
          "ready": true
        },
        "offset": 0,
        "size": 3
      },
      "rc": [
        {
          "id": "#1937:7",
          "class_name": "RcTm66OrderExpertiseProtocol",
          "patient_id": "#68:44221",
          "ehr_id": "#1052:44221",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-27 12:57:29"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-27 12:57:29",
          "rc_tm66_order_expertise_protocol": {
            "order_id": "#1945:50",
            "result": {
              "code": "НАРУШЕНИЙ_НЕТ",
              "caption": "Нарушений нет"
            },
            "description": "Полное соответствие",
            "pdf_id": "#1588:7174"
          }
        },
        {
          "id": "#1938:2",
          "class_name": "RcTm66OrderExpertiseProtocol",
          "patient_id": "#68:44971",
          "ehr_id": "#1052:44971",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-27 12:59:40"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-27 12:59:40",
          "rc_tm66_order_expertise_protocol": {
            "order_id": "#1945:49",
            "result": {
              "code": "НАРУШЕНИЙ_НЕТ",
              "caption": "Нарушений нет"
            },
            "description": "Полное соответствие",
            "pdf_id": "#1590:7094"
          }
        }
      ],
      "size": 2
    }
  ]
}
```