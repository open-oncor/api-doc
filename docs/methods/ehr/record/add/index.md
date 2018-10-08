[Работа с заболеваниями пациента](../../index.md)
=====================================

### ![POST](../../../../img/post.png) /ehr/record/add
* **Request:** [Rc](../../../../types/types.md#rc) **record** <patient_id, ehr_id, rc>
* **Response:** [[Rc](../../../../types/types.md#rc)]

Добавляет запись в указанное заболевание.

В запросе передаётся:

[Rc](../../../../types/types.md#rc):
* required patient_id
* required ehr_id
* one of ([RcDoc](../../../../types/types.md#rcrcdoc), [RcReferral](../../../../types/types.md#rcrcreferral), 
[RcOper](../../../../types/types.md#rcrcoper), [RcHorm](../../../../types/types.md#rcrchorm), 
[RcChem](../../../../types/types.md#rcrcchem), [RcRay](../../../../types/types.md#rcrcray))

В ответе передаётся [Rc](../../../../types/types.md#rc).

* **[Пример добавления записи RcChem](examples/RcChem/add.md)**
* **[Пример добавления записи RcDz](examples/RcDz/add.md)**
* **[Пример добавления записи RcHorm](examples/RcHorm/add.md)**
* **[Пример добавления записи RcOper](examples/RcOper/add.md)**
* **[Пример добавления записи RcRay](examples/RcRay/add.md)**