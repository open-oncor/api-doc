Работа с ЭМЗ
============

### ![GET](../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types/types.md#ehr)
* **Response:** [[EHR](../../types/types.md#ehr)]

Возвращает список ЭМЗ для пациента с идентификатором [patient_id](../../types/types.md#ehr).

В ответе передаётся массив объектов [EHR](../../types/types.md#ehr).

**[Examples](getList/examples/getList.md)**

---

### ![GET](../../img/get.png) /ehr/getActive`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types/types.md#ehr)
* **Response:** [[EHR](../../types/types.md#ehr)]

Возвращает активную ЭМЗ для пациента с идентификатором [patient_id](../../types/types.md#ehr).

В ответе передаётся массив с единственным объектом - [EHR](../../types/types.md#ehr) или пустой, если у пациента нет активных ЭМЗ.

**[Examples](getActive/examples/getActive.md)**

---

### ![POST](../../img/post.png) [/ehr/add](add/index.md)
* **Request:** [EHR](../../types/types.md#ehr) **ehr <patient_id>**
* **Response ```200```:** [[EHR](../../types/types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../types/types.md#errorresult)

Добавляет ЭМЗ. В случае отсутствия пациента, к которому относится ЭМЗ, возвращается ошибка.

В запросе передаётся объект:

[EHR](../../types/types.md#ehr)
* required patient_id

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[EHR](../../types/types.md#ehr) с заполненым полем [id](../../types/types.md#ehr).

**[Examples](add/examples/add.md)**

---

### ![POST](../../img/post.png) [/ehr/record/add](record/add/index.md)
* **Request:** [Rc](../../types/types.md#rc) **record <patient_id, ehr_id, rc>**
* **Response:** [[Rc](../../types/types.md#rc)]

Добавляет запись в ЭМЗ.

В запросе передаётся

[Rc](../../types/types.md#rc):
* required patient_id
* required ehr_id
* one of ([RcDoc](../../types/types.md#rcrcdoc), [RcReferral](../../types/types.md),  [RcOper](../../types/types.md#rcrcoper))

В ответе передаётся [Rc](../../types/types.md#rc).

* **[Пример добавления записи RcChem](record/add/examples/RcChem/add.md)**
* **[Пример добавления записи RcDz](record/add/examples/RcDz/add.md)**
* **[Пример добавления записи RcHorm](record/add/examples/RcHorm/add.md)**
* **[Пример добавления записи RcOper](record/add/examples/RcOper/add.md)**
* **[Пример добавления записи RcRay](record/add/examples/RcRay/add.md)**