# Удаление записей

## Удаление записи из указанного заболевания

### ![POST](../../../../img/post.png) /ehr/record/delete
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) 
* **Response:** Пустой массив или информация об ошибке




### Пример http
 
 **Request**
 
 POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/delete HTTP/1.1`  
 `X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
 `Content-Type: application/json`
 
 ```json
 {
     "record":{
         "id":"#881:11797",
         "patient_id":"#65:10693",
         "ehr_id": "#64:163"
     }
 }
 ```
 
 **Response**
 ```json
 {
   "result": []
 }
 ```

## Удаление указанного заболевания

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/delete HTTP/1.1`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`

 ```json
{
     "ehr":{
          "id":"#877:54362"
     }
}
 ```
**Response**
 ```json
 {
   "result": []
 }
 ```