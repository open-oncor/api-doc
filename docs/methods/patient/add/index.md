### Добавление пациента

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types/types.md#com.siams.med.api.Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../../types/types.md#com.siams.med.api.Patient)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#com.siams.med.api.ErrorResult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

#### Примеры
**[http](examples/add.md)**
**[java](examples/addJava.md)**
