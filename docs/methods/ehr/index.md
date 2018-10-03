Работа с ЭМЗ
============

<a name="getList"/>

### ![GET](../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#ehr)
* **Response:** [[EHR](../../types.md#ehr)]

Возвращает список ЭМЗ для пациента с идентификатором [patient_id](../../types.md#ehr).

В ответе передаётся массив объектов [EHR](../../types.md#ehr).

---

<a name="getActive"/>

### ![GET](../../img/get.png) /ehr/getActive`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#ehr)
* **Response:** [[EHR](../../types.md#ehr)]

Возвращает активную ЭМЗ для пациента с идентификатором [patient_id](../../types.md#ehr).

В ответе передаётся массив с единственным объектом - [EHR](../../types.md#ehr) или пустой, если у пациента нет активных ЭМЗ.

---

### ![POST](../../img/post.png) [/ehr/add](add/index.md)
* **Request:** [EHR](../../types.md#ehr) **ehr** <patient_id>
* **Response ```200```:** [[EHR](../../types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../types.md#errorresult)

Добавляет ЭМЗ. В случае отсутствия пациента, к которому относится ЭМЗ, возвращается ошибка.

В запросе передаётся объект:

[EHR](../../types.md#ehr)
* required patient_id

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[EHR](../../types.md#ehr) с заполненым полем [id](../../types.md#ehr).

**[Examples](add/examples/add.md)**

---

### ![POST](../../img/post.png) [/ehr/record/add](record/add/index.md)
* **Request:** [Rc](../../types.md#rc) **record** <patient_id, ehr_id, rc>
* **Response:** [[Rc](../../types.md#rc)]

Добавляет запись в ЭМЗ.

В запросе передаётся

[Rc](../../types.md#rc):
* required patient_id
* required ehr_id
* one of ([RcDoc](../../types.md#rcrcdoc), [RcReferral](../../types.md),
 [RcAppointment](../../types.md#rcrcappointment), [RcOper](../../types.md#rcrcoper))

В ответе передаётся [Rc](../../types.md#rc).

**[Examples](record/add/examples/add.md)**