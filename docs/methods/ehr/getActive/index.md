[Работа с заболеваниями пациента](../index.md)
===========================

### ![GET](../../../img/get.png) /ehr/getActive`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../types/types.md#ehr)
* **Response:** [[EHR](../../../types/types.md#ehr)]

Устаревший метод. Возвращает активное заболевание пациента с идентификатором [patient_id](../../../types/types.md#ehr).

В ответе передаётся массив с единственным объектом - [EHR](../../../types/types.md#ehr) или пустой, 
если у пациента нет активных заболеваний.

**[Примеры](examples/getActive.md)**