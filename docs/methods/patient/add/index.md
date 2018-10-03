[Работа с пациентами](../index.md)
=====================================

### ![POST](../../../img/post.png) /patient/add
* **Request:** [Patient](../../../types.md#Patient) **patient** <first_name, last_name, middle_name, birth_day>
* **Response ```200```:** [[Patient](../../../types.md#Patient)]
* **Response ```422```:** [ErrorResult](../../../types.md#errorresult)

Добавляет пациента с проверкой дублей. В случае наличия пациента с такими данными возвращается ошибка.

В запросе передаётся объект:

[Patient](../../../types.md#Patient)
* first_name
* last_name
* middle_name
* birth_day
 
В случае успешного добавления, в ответе будет массив с единственным объектом - [Patient](../../../types.md#Patient) 
с заполненым полем [id](../../../types.md#Patient).

**[Examples](examples/add.md)**