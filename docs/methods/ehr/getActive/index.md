[Работа с ЭМЗ](../index.md)
===========================

### ![GET](../../../img/get.png) /ehr/getActive`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../types/types.md#ehr)
* **Response:** [[EHR](../../../types/types.md#ehr)]

Возвращает активную ЭМЗ для пациента с идентификатором [patient_id](../../../types/types.md#ehr).

В ответе передаётся массив с единственным объектом - [EHR](../../../types/types.md#ehr) или пустой, 
если у пациента нет активных ЭМЗ.

**[Примеры](examples/getActive.md)**