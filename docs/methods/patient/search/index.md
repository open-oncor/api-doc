[Работа с пациентами](../index.md)
==================================

### ![POST](../../../img/post.png) /patient/search
* **Request:** [PatientQuery](../../../types.md#PatientQuery) **patient_query** <first_name, last_name, middle_name, birth_day>
* **Response:** [[Patient](../../../types.md#Patient)]

Возвращает список пациентов в соответствии с запросом.

В запросе передаётся объект:

[PatientQuery](../../../types.md#PatientQuery)
* required first_name
* required last_name
* required middle_name
* required birth_day

В ответе - массив объектов [Patient](../../../types.md#Patient), пустой, если не найдено ни одного пациента.

**[Examples](examples/search.md)**