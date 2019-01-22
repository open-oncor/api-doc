### Удаление записи из указанного пациента

### ![POST](../../../../img/post.png) /patient/record/delete
* **Request:** [Rc](../../../../types/types.md#com.siams.med.api.Rc) 
```json
{
    "record":{
        "id":"#881:11797",
        "patient_id":"#65:10693"
    }
}
```

* **Response:** Пустой массив или информация об ошибке
```json
{
  "result": [
  ]
}
```


#### Примеры
 **[http](examples/delete.md) [java](examples/deleteJava.md)**
