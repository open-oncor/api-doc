Работа с пациентами
=======================

### ![GET](../../img/get.png) /patient/get`?id={patient_id}`
* **URL parameter:** [id](../../types/types.md#com.siams.med.api.Patient)
* **Response:** [[Patient](../../types/types.md#com.siams.med.api.Patient)]

Возвращает объект типа [Patient](../../types/types.md#com.siams.med.api.Patient).

В ответе передаётся массив с единственным объектом - [Patient](../../types/types.md#com.siams.med.api.Patient).

**[Примеры](get/examples/get.md)**

---

### ![POST](../../img/post.png) [/patient/add](add/index.md)
* **Request:** [Patient](../../types/types.md#com.siams.med.api.Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../types/types.md#com.siams.med.api.Patient)]
* **Response ```422```:** [ErrorResult](../../types/types.md#com.siams.med.api.ErrorResult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

В запросе передаётся объект:

[Patient](../../types/types.md#com.siams.med.api.Patient)
* required first_name
* required last_name
* required middle_name
* required birth_day

В случае успешного добавления, в ответе будет массив с единственным объектом - 
[Patient](../../types/types.md#com.siams.med.api.Patient) с заполненым полем [id](../../types/types.md#com.siams.med.api.Patient).

**[Примеры](add/examples/add.md)**

---

### ![POST](../../img/post.png) [/patient/search](search/index.md)
* **Request:** [PatientQuery](../../types/types.md#com.siams.med.api.PatientQuery) **patient_query** <first_name, last_name, middle_name, birth_day>
* **Response:** [[Patient](../../types/types.md#com.siams.med.api.Patient)]

Возвращает список пациентов в соответствии с запросом.

В запросе передаётся объект:

[PatientQuery](../../types/types.md#com.siams.med.api.PatientQuery)
* required first_name
* required last_name
* required middle_name
* required birth_day

В ответе - массив объектов [Patient](../../types/types.md#com.siams.med.api.Patient), пустой, если не найдено ни одного пациента.

**[Примеры](search/examples/search.md)**

---

### ![GET](../../img/get.png) /patient/forceAdd
* **Request:** [Patient](../../types/types.md#com.siams.med.api.Patient) patient
* **Response:** [[Patient](../../types/types.md#com.siams.med.api.Patient)]

Добавляет пациента безусловно.

В запросе передаётся объект - [Patient](../../types/types.md#com.siams.med.api.Patient). 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../types/types.md#com.siams.med.api.Patient) 
с заполненым полем id.

**[Примеры](forceAdd/examples/forceAdd.md)**

---

### ![POST](../../img/post.png) /patient/update
* **Request:** [PatientUpdate](../../types/types.md#com.siams.med.api.PatientUpdate) **patient <id, code>**
* **Response:** [[Patient](../../types/types.md#com.siams.med.api.Patient)]

Обновляет данные пациента

В запросе передаётся объект - [PatientUpdate](../../types/types.md#com.siams.med.api.PatientUpdate). 

В ответе - объект [Patient](../../types/types.md#com.siams.med.api.Patient).

**[Примеры](update/examples/update.md)**

---

### ![POST](../../img/post.png) /patient/record/add
* **Request:** [Rc](../../types/types.md#com.siams.med.api.Rc)
* **Response:** [Rc](../../types/types.md#com.siams.med.api.Rc)

Добавляет запись пациенту. В запросе передаётся объект - [Rc](../../types/types.md#com.siams.med.api.Rc).

В ответе - [Rc](../../types/types.md#com.siams.med.api.Rc).

**[Примеры](record/add/examples/RcRegIn/add.md)**

---

### ![POST](../../img/post.png) /patient/RcAppointment/add
* **Request:** [Rc](../../types/types.md#com.siams.med.api.Rc) record
* **Response:** [Rc](../../types/types.md#com.siams.med.api.Rc)

Добавляет предварительную запись. В запросе передаётся объект - [Rc](../../types/types.md#com.siams.med.api.Rc). 

В ответе - [Rc](../../types/types.md#com.siams.med.api.Rc).

**[Примеры](RcAppointment/add/examples/add.md)**

---

### ![GET](../../img/get.png) /patient/record/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../types/types.md#com.siams.med.api.Rc)]

Возвращает список записей для пациента с идентификатором [patient_id](../../types/types.md#com.siams.med.api.Rc).

В ответе передаётся массив объектов [Rc](../../types/types.md#com.siams.med.api.Rc).

**[Примеры](record/getList/examples/getList.md)**

---

### ![GET](../../img/get.png) /patient/RcReferralRL/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../types/types.md#com.siams.med.api.Rc)]

Возвращает список направлений для пациента с идентификатором [patient_id](../../types/types.md#com.siams.med.api.Rc).

В ответе передаётся массив объектов [Rc](../../types/types.md#com.siams.med.api.Rc).

**[Примеры](RcReferralRl/getList/examples/getList.md)**