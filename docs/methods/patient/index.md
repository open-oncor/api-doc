Работа с пациентами
=======================

<a name="get"/>

### ![GET](../../img/get.png) /patient/get`?id={patient_id}`
* **URL parameter:** [id](../../types.md#Patient)
* **Response:** [[Patient](../../types.md#Patient)]

Возвращает объект типа [Patient](../../types.md#Patient).

В ответе передаётся массив с единственным объектом - [Patient](../../types.md#Patient).

---

### ![POST](../../img/post.png) [/patient/add](add/index.md)
* **Request:** [Patient](../../types.md#Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../types.md#Patient)]
* **Response ```422```:** [ErrorResult](../../types.md#errorresult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

В запросе передаётся объект:

[Patient](../../types.md#Patient)
* required first_name
* required last_name
* required middle_name
* required birth_day

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[Patient](../../types.md#Patient) с заполненым полем [id](../../types.md#Patient).

**[Examples](add/examples/add.md)**

---

### ![POST](../../img/post.png) [/patient/search](search/index.md)
* **Request:** [PatientQuery](../../types.md#PatientQuery) **patient_query** <first_name, last_name, middle_name, birth_day>
* **Response:** [[Patient](../../types.md#Patient)]

Возвращает список пациентов в соответствии с запросом.

В запросе передаётся объект:

[PatientQuery](../../types.md#PatientQuery)
* required first_name
* required last_name
* required middle_name
* required birth_day

В ответе - массив объектов [Patient](../../types.md#Patient), пустой, если не найдено ни одного пациента.

**[Examples](search/examples/search.md)**

---

<a name="forceAdd"/>

### ![GET](../../img/get.png) /patient/forceAdd
* **Request:** [Patient](../../types.md#Patient)
* **Response:** [[Patient](../../types.md#Patient)]

Добавляет пациента безусловно.

В запросе передаётся объект - [Patient](../../types.md#Patient). 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../types.md#Patient) с заполненым полем id.

---

<a name="update"/>

### ![POST](../../img/post.png) /patient/update
* **Request:** [PatientUpdate](../../types.md#patientupdate)
* **Response:** [[Patient](../../types.md#Patient)]

Обновляет данные пациента

В запросе передаётся объект - [PatientUpdate](../../types.md#patientupdate). 

В ответе - объект [Patient](../../types.md#Patient).

---

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

### ![GET](../../img/get.png) /patient/record/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#rc)
* **Response:** [[Rc](../../types.md#rc)]

Возвращает список записей для пациента с идентификатором [patient_id](../../types.md#rc).

В ответе передаётся массив объектов [Rc](../../types.md#rc).

**[Examples](record/getList/examples/getList.md)**

---

<a name="RcRefferralRcGetList"/>

### ![GET](../../img/get.png) /patient/RcReferralRL/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types.md#rc)
* **Response:** [[Rc](../../types.md#rc)]

Возвращает список направлений для пациента с идентификатором [patient_id](../../types.md#rc).

В ответе передаётся массив объектов [Rc](../../types.md#rc).