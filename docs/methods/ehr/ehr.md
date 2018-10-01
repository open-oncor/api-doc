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

<a name="add"/>

### ![POST](../../img/post.png) /ehr/add
* **Request:** [patient_id](../../types.md#ehr)
* **Response ```200```:** [[EHR](../../types.md#ehr)]
* **Response ```422```:** [ErrorResult](../../types.md#errorresult)

Добавляет ЭМЗ. В случае отсутствия пациента, к которому относится ЭМЗ, возвращается ошибка.

В запросе передаётся объект - [EHR](../../types.md#ehr).
В случае успешного добавления, в ответе будет массив с единственным объектом - [EHR](../../types.md#ehr) с заполненым полем [id](../../types.md#ehr).
