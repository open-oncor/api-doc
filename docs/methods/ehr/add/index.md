[Работа с ЭМЗ](../index.md)
=====================================================

<a name="add"/>

### ![POST](../../../img/post.png) /ehr/add
* **Request:** [EHR](../../../types.md#ehr) **ehr** <patient_id>
* **Response ```200```:** [[EHR](../../../types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../../types.md#errorresult)

Добавляет ЭМЗ. В случае отсутствия пациента, к которому относится ЭМЗ, возвращается ошибка.

В запросе передаётся объект:

[EHR](../../../types.md#ehr)
* required patient_id

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[EHR](../../../types.md#ehr) с заполненым полем [id](../../../types.md#ehr).

**[Examples](examples/add.md)**