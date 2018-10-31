### Регистрация заболевания пациента

### ![POST](../../../img/post.png) /ehr/add
* **Request:** [EHR](../../../types/types.md#com.siams.med.api.EHR) **ehr** <patient_id>
* **Response ```200```:** [[EHR](../../../types/types.md#com.siams.med.api.EHR)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#com.siams.med.api.ErrorResult)

Регистрирует новое заболевание для пациента.  

#### Примеры
**[http](examples/add.md)**
**[java](examples/addJava.md)**