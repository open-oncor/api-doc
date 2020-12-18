# Поиск документов "Экспертиза качества DICOM"

1. Стартуем поиск документов "Экспертиза качества DICOM"
**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/search/start/RcTm66OrderExpertiseDicomQuery`  
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
      "id": "5c78a4f4-8c6e-42ba-a5dc-304149f646c5"
    }
  ]
}
```
2. Получение списка документов "Экспертиза качества DICOM"  
**Request**
POST `https://demo.onco-reg.ru/api/1.0/json/search/get/RecordsPage`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
  "page":{
    "job":{
      "id":"5c78a4f4-8c6e-42ba-a5dc-304149f646c5"
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
          "id": "5c78a4f4-8c6e-42ba-a5dc-304149f646c5",
          "ready": true
        },
        "offset": 0,
        "size": 3
      },
      "rc": [
        {
          "id": "#1961:7",
          "class_name": "RcTm66OrderExpertiseDicom",
          "patient_id": "#68:44221",
          "ehr_id": "#1052:44221",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-27 12:57:29"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-27 12:57:29",
          "rc_tm66_order_expertise_dicom": {
            "order_id": "#1945:50",
            "result": {
              "code": "НАРУШЕНИЙ_НЕТ",
              "caption": "Нарушений нет"
            },
            "description": "Нет технических замечаний",
            "pdf_id": "#1587:7232"
          }
        },
        {
          "id": "#1962:2",
          "class_name": "RcTm66OrderExpertiseDicom",
          "patient_id": "#68:44971",
          "ehr_id": "#1052:44971",
          "published": {
            "user_id": "#962:280",
            "time": "2020-10-27 12:59:40"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-10-27 12:59:40",
          "rc_tm66_order_expertise_dicom": {
            "order_id": "#1945:49",
            "result": {
              "code": "НАРУШЕНИЙ_НЕТ",
              "caption": "Нарушений нет"
            },
            "description": "Нет технических замечаний",
            "pdf_id": "#1589:7131"
          }
        }
      ],
      "size": 2
    }
  ]
}
```

