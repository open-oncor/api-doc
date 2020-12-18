# Поиск докуметов "Заключение эксперта ДЭЗО"

### Пример http

1. Стартуем поиск документов "Заключение эксперта ДЭЗО"
   
**Request**
POST `https://demo.onco-reg.ru/api/1.0/json/search/start/RcTm66OrderConclusionQuery`  
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
      "id": "f7f04776-1567-43e3-a385-1858f525a7d3"
    }
  ]
}
```

2.  Получение списка найденных докуметов "Заключение эксперта ДЭЗО"

POST `https://demo.onco-reg.ru/api/1.0/json/search/get/RecordsPage`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
  "page": {
    "job": {
      "id": "f7f04776-1567-43e3-a385-1858f525a7d3"
    },
    "offset": 0,
    "size": 3
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
          "id": "f7f04776-1567-43e3-a385-1858f525a7d3",
          "ready": true
        },
        "offset": 0,
        "size": 3
      },
      "rc": [
        {
          "id": "#1985:11",
          "class_name": "RcTm66OrderConclusion",
          "patient_id": "#72:37903",
          "ehr_id": "#1056:37903",
          "published": {
            "user_id": "#962:280",
            "time": "2020-09-25 14:06:40"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-09-25 14:06:40",
          "rc_tm66_order_conclusion": {
            "order_id": "#1950:3",
            "conclusion": {
              "code": "ЗАКЛЮЧЕНИЕ_СОВПАДАЕТ",
              "caption": "Заключение эксперта совпадает с направленным заключением"
            },
            "description": "Заключение эксперта совпадает с направленным заключением",
            "pdf_id": "#1592:5249"
          }
        },
        {
          "id": "#1985:12",
          "class_name": "RcTm66OrderConclusion",
          "patient_id": "#68:44221",
          "ehr_id": "#1052:44221",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-09 16:18:50"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-09 16:18:50",
          "rc_tm66_order_conclusion": {
            "order_id": "#1945:50",
            "conclusion": {
              "code": "ДИАГНОЗ_ПОДТВЕРЖДЕН",
              "caption": "Диагноз подтвержден"
            },
            "description": "Диагноз подтвержден",
            "pdf_id": "#1591:5953"
          }
        },
        {
          "id": "#1985:13",
          "class_name": "RcTm66OrderConclusion",
          "patient_id": "#66:44978",
          "ehr_id": "#1050:44978",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-13 12:33:44"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-13 12:33:44",
          "rc_tm66_order_conclusion": {
            "order_id": "#1946:29",
            "conclusion": {
              "code": "ИЗМЕНЕНИЕ_ТАКТИКИ_ТРЕБУЕТСЯ",
              "caption": "Требуется изменение тактики лечения"
            },
            "description": "Требуется изменение тактики лечения",
            "pdf_id": "#1587:6272"
          }
        }
      ],
      "size": 3
    }
  ]
}
```

   