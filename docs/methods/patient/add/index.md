### Добавление пациента

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types/types.md#Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../../types/types.md#Patient)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#errorresult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

#### Примеры
**[http](examples/add.md)**
**[java](examples/addJava.md)**
