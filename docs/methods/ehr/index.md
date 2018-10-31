Работа с заболеваниями пациента
===============================

### ![GET](../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types/types.md#com.siams.med.api.EHR)
* **Response:** [[EHR](../../types/types.md#com.siams.med.api.EHR)]

Возвращает список заболеваний пациента с идентификатором [patient_id](../../types/types.md#com.siams.med.api.EHR).

В ответе передаётся массив объектов [EHR](../../types/types.md#com.siams.med.api.EHR).

**[Примеры](getList/examples/getList.md)**

---

### ![POST](../../img/post.png) [/ehr/add](add/index.md)
* **Request:** [EHR](../../types/types.md#com.siams.med.api.EHR) **ehr <patient_id>**
* **Response ```200```:** [[EHR](../../types/types.md#com.siams.med.api.EHR)]
* **Response ```422```:** [ErrorResult](../../types/types.md#com.siams.med.api.ErrorResult)

Регистрирует новое заболевание пациенту. В случае отсутствия пациента, к которому относится заболевание, возвращается ошибка.

В запросе передаётся объект:

[EHR](../../types/types.md#com.siams.med.api.EHR)
* required patient_id

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[EHR](../../types/types.md#com.siams.med.api.EHR) с заполненым полем [id](../../types/types.md#com.siams.med.api.EHR).

**[Примеры](add/examples/add.md)**

---

### ![POST](../../img/post.png) [/ehr/record/add](record/add/index.md)
* **Request:** [Rc](../../types/types.md#com.siams.med.api.Rc) **record <patient_id, ehr_id, rc>**
* **Response:** [[Rc](../../types/types.md#com.siams.med.api.Rc)]

Добавляет запись, привязанную к заболеванию пациента.

В запросе передаётся

[Rc](../../types/types.md#com.siams.med.api.Rc):
* required patient_id
* required ehr_id
* one of ([RcDoc](../../types/types.md#rcrcdoc), [RcReferral](../../types/types.md),  [RcOper](../../types/types.md#rcrcoper))

В ответе передаётся [Rc](../../types/types.md#com.siams.med.api.Rc).

* **[Пример добавления записи RcChem](record/add/examples/RcChem/add.md)**
* **[Пример добавления записи RcDz](record/add/examples/RcDz/add.md)**
* **[Пример добавления записи RcHorm](record/add/examples/RcHorm/add.md)**
* **[Пример добавления записи RcOper](record/add/examples/RcOper/add.md)**
* **[Пример добавления записи RcRay](record/add/examples/RcRay/add.md)**