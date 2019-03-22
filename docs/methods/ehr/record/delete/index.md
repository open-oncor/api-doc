## Удаление записи из указанного заболевания

### ![POST](../../../../img/post.png) /ehr/record/delete
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) 
* **Response:** Пустой массив или информация об ошибке




### Пример http
 
 **Request**
 
 POST `http://dev.onco-reg.ru/api/1.0/json/ehr/record/delete HTTP/1.1`
 
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
   "result": [
   ]
 }
 ```
 
### Пример java
 
 ```java
 class Demo {
     public static void main(String... args) { 
         client.deleteEhrRecord(Records.Rc.newBuilder()
                                .setId(edrRc.getId())
                                .setPatientId(edrRc.getPatientId())
                                .setEhrId(edrRc.getEhrId())
                                .build());
     }
 }
 ```