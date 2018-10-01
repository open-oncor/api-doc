Работа с записями пациентов
===========================

<a name="add"/>

### ![POST](../../img/post.png) /patient/record/add
* **Request:** [Rc](../../types.md#rc)
* **Response:** [Rc](../../types.md#rc)

Добавляет запись пациенту. В запросе передаётся объект - [Rc](../../types.md#rc).

В ответе - [Rc](../../types.md#rc).

---

<a name="RcAppointmentAdd"/>

### ![POST](../../img/post.png) /patient/RcAppointment/add
* **Request:** [Rc](../../types.md#rc)
* **Response:** [Rc](../../types.md#rc)

Добавляет предварительную запись. В запросе передаётся объект - [Rc](../../types.md#rc). 

В ответе - [Rc](../../types.md#rc).

---

<a name="getList"/>

### ![GET](../../img/get.png) /patient/record/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#rc)
* **Response:** [[Rc](../../types.md#rc)]

Возвращает список записей для пациента с идентификатором [patient_id](../../types.md#rc).

В ответе передаётся массив объектов [Rc](../../types.md#rc).

---

<a name="RcRefferralRcGetList"/>

### ![GET](../../img/get.png) /patient/RcReferralRL/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#rc)
* **Response:** [[Rc](../../types.md#rc)]

Возвращает список направлений для пациента с идентификатором [patient_id](../../types.md#rc).

В ответе передаётся массив объектов [Rc](../../types.md#rc).