[Работа с ЭМЗ](../../index.md)
=====================================

<a name="add"/>

### ![POST](../../../../img/post.png) /ehr/record/add
* **Request:** [Rc](../../../../types.md#rc) **record** <patient_id, ehr_id, rc>
* **Response:** [[Rc](../../../../types.md#rc)]

Добавляет запись в ЭМЗ.

В запросе передаётся:

[Rc](../../../../types.md#rc):
* required patient_id
* required ehr_id
* one of ([RcDoc](../../../../types.md#rcrcdoc), [RcReferral](../../../../types.md),
 [RcAppointment](../../../../types.md#rcrcappointment), [RcOper](../../../../types.md#rcrcoper))

В ответе передаётся [Rc](../../../../types.md#rc).

**[Examples](examples/add.md)**