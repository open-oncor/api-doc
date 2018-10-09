## Регистрация заболевания пациента

### ![POST](../../../img/post.png) /ehr/add
* **Request:** [EHR](../../../types/types.md#ehr) **ehr** <patient_id>
* **Response ```200```:** [[EHR](../../../types/types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#errorresult)

Регистрирует новое заболевание для пациента. 

#### Примеры
**[http](examples/add.md)**
**[java](examples/addJava.md)**