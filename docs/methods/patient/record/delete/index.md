## Удаление записи из указанного пациента

### ![POST](../../../../img/post.png) /patient/record/delete
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) 
* **Response:** Пустой массив или информация об ошибке



### Пример http
 
 **Request**
 
 POST `https://demo.onco-reg.ru/api/1.0/json/patient/record/delete HTTP/1.1`  
 `X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
 `Content-Type: application/json`
 
 ```json
 {
     "record":{
         "id":"#881:11797",
         "patient_id":"#65:10693"
     }
 }
 ```
 
 **Response**
 ```json
 {
   "result": [
   ]
 }
 ```
