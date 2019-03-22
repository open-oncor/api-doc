## Удаление записи из указанного пациента

### ![POST](../../../../img/post.png) /patient/record/delete
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) 
* **Response:** Пустой массив или информация об ошибке



### Пример http
 
 **Request**
 
 POST `http://dev.onco-reg.ru/api/1.0/json/patient/record/delete HTTP/1.1`
 
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

 
 
 
### Пример java
 
 ```java
 class Demo {
     public static void main(String... args) { 
         client.deletePatientRecord(Records.Rc.newBuilder()
                 .setId(ptnRc.getId())
                 .setPatientId(ptnRc.getPatientId())
                 .build());
     }
 }
 ```
