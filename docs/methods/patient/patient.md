Работа с пациентами
=======================

<a name="get"/>

### ![GET](../../img/get.png) /patient/get`?id={patient_id}`
* **URL parameter:** [id](../../types.md#Patient)
* **Response:** [[Patient](../../types.md#Patient)]

Возвращает объект типа [Patient](../../types.md#Patient).

В ответе передаётся массив с единственным объектом - [Patient](../../types.md#Patient).

---

<a name="add"/>

### ![POST](../../img/post.png) /patient/add
* **Request:** [Patient](../../types.md#Patient)
* **Response ```200```:** [[Patient](../../types.md#Patient)]
* **Response ```422```:** [ErrorResult](../../types.md#errorresult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

В запросе передаётся объект - [Patient](../../types.md#Patient). 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../types.md#Patient) с заполненым полем [id](../../types.md#Patient).

[Examples](add/examples/add.md)

---

<a name="search"/>

### ![POST](../../img/post.png) /patient/search
* **Request:** [PatientQuery](../../types.md#PatientQuery)
* **Response:** [[Patient](../../types.md#Patient)]

Возвращает список пациентов в соответствии с запросом.

В запросе передаётся объект - [PatientQuery](../../types.md#PatientQuery). 
В ответе - массив объектов [Patient](../../types.md#Patient), пустой, если не найдено ни одного пациента.

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
