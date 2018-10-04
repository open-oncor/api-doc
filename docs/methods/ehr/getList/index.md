[Работа с ЭМЗ](../index.md)
===========================

### ![GET](../../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../types/types.md#ehr)
* **Response:** [[EHR](../../../types/types.md#ehr)]

Возвращает список ЭМЗ для пациента с идентификатором [patient_id](../../../types/types.md#ehr).

В ответе передаётся массив объектов [EHR](../../../types/types.md#ehr).

**[Examples](examples/getList.md)**