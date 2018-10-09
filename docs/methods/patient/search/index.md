[Работа с пациентами](../index.md)
==================================

### ![POST](../../../img/post.png) /patient/search
* **Request:** [PatientQuery](../../../types/types.md#PatientQuery) **patient_query** <first_name, last_name, middle_name, birth_day>
* **Response:** [[Patient](../../../types/types.md#Patient)]

Возвращает массив пациентов в соответствии с запросом или пустой массив, если не найдено ни одного пациента. 


#### Примеры
**[http](examples/search.md)**
**[java](examples/searchJava.md)**
