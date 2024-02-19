## Добавление черновика записи "Протокол запущенного случая" в указанное заболевание (RcNeglectedCase)

### ![POST](../../../../../img/post.png) /ehr/record/put
* **Request:** [RcNeglectedCase](../../../../../types/types.md#com.siams.med.api.Rc.RcNeglectedCase) **record** <patient_id, ehr_id, RcChem>
* **Response:** [[RcNeglectedCase](../../../../../types/types.md#com.siams.med.api.Rc.RcNeglectedCase)]

Черновик записи "Протокол запущенного случая" добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание и становится доступной для дозаполнения и публикации врачом из интерфейса системы.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/put HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`  

```json
{
  "record": {
    "patient_id": "{{ptnId}}",
    "ehr_id": "{{ehrId}}",
    "time_rc": "1999-01-21",
    "draft": true,
    "rc_neglected_case": {
      "number": "№157",
      "date": "1999-02-14",
      "first_sign_date": "1999-01-14",
      "first_request_date": "1999-01-10",
      "first_request_lpu_id": "{{lpu1}}",
      "first_dz_date": "1999-01-14",
      "first_dz_lpu_id": "{{lpu1}}",
      "history": "до 10.1.99 за мед. помощью не обращалась",
      "review_data": "Взята гистология",
      "conference_date": "1999-02-14",
      "conference_lpu_id": "{{lpu1}}",
      "conclusion": "продолжить активно информировать население по вопросам профилактики и раннего выявления новообразований, ведение ЗОЖ,..."
    }
  }
}
```

**Response**
```json
{
  "result": [
    {
      "id": "#1759:34",
      "class_name": "RcNeglectedCase",
      "patient_id": "#71:30716",
      "ehr_id": "#878:69515",
      "org_unit_id": "#993:0",
      "draft": true,
      "time_rc": "1999-01-21 00:00:00",
      "meta": "{}",
      "rc_neglected_case": {
        "number": "№157",
        "date": "1999-02-14",
        "first_sign_date": "1999-01-14",
        "first_request_date": "1999-01-10",
        "first_request_lpu_id": "#993:6",
        "first_dz_date": "1999-01-14 00:00:00",
        "first_dz_lpu_id": "#993:6",
        "history": "до 10.1.99 за мед. помощью не обращалась",
        "review_data": "Взята гистология",
        "conference_date": "1999-02-14",
        "conference_lpu_id": "#993:6",
        "conclusion": "продолжить активно информировать население по вопросам профилактики и раннего выявления новообразований, ведение ЗОЖ,..."
      }
    }
  ]
}
```

