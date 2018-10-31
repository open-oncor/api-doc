### Добавление диагноза в указанное заболевание (RcDz)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcDz](../../../../../types/types.md#com.siams.med.api.Dz) **record** <patient_id, ehr_id, RcDz>
* **Response:** [[RcDz](../../../../../types/types.md#com.siams.med.api.Dz)]

Диагноз добавляется как запись Rc в указанное заболевание. Есди такой диагноз уже зарегистрирован у пациента ранее, метод вернёт ошибку.

#### Примеры
**[http](../examples/RcDz/add.md) [java](../examples/RcDz/addJava.md)**
