[Работа с ЭМЗ](../index.md)
=====================================================

<a name="add"/>

### ![POST](../../../img/post.png) /ehr/add
* **Request:** [EHR](../../../types/types.md#ehr) **ehr** <patient_id>
* **Response ```200```:** [[EHR](../../../types/types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#errorresult)

Добавляет ЭМЗ. В случае отсутствия пациента, к которому относится ЭМЗ, возвращается ошибка.

В запросе передаётся объект:

[EHR](../../../types/types.md#ehr)
* required patient_id

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[EHR](../../../types/types.md#ehr) с заполненым полем [id](../../../types/types.md#ehr).

**[Examples](examples/add.md)**