[Работа с пациентами](../index.md)
==================================

### ![GET](../../../img/get.png) /patient/forceAdd
* **Request:** [Patient](../../../types/types.md#Patient) patient
* **Response:** [[Patient](../../../types/types.md#Patient)]

Добавляет пациента безусловно.

В запросе передаётся объект - [Patient](../../../types/types.md#Patient). 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../../types/types.md#Patient) 
с заполненым полем id.

**[Примеры](examples/forceAdd.md)**
**[Примеры кода](examples/forceAddCode.md)**