[Работа с пациентами](../index.md)
==================================

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types/types.md#Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../../types/types.md#Patient)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#errorresult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

В запросе передаётся объект:

[Patient](../../../types/types.md#Patient)
* first_name
* last_name
* middle_name
* birth_day
 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../../types/types.md#Patient) 
с заполненым полем [id](../../../types/types.md#Patient).

**[Примеры](examples/add.md)**
**[Примеры кода](examples/addCode.md)**