Работа с метаданными
====================

### ![POST](../../img/post.png) /meta/query
* **Request:** [Query](../../types/types.md#com.siams.med.api.Query) query
* **Response:** [[Meta.proto](../../types/types.md#metaproto)]

Возвращает список метаданных [Meta.proto](../../types/types.md#metaproto) 
для объектов с указанными [id](../../types/types.md#metaproto)

**[Примеры](query/examples/query.md)**

---

### ![POST](../../img/post.png) /meta/update
* **Request:** [Update](../../types/types.md#com.siams.med.api.Update) update
* **Response:** [[Meta.proto](../../types/types.md#metaproto)]

Обновляет метаданные [Meta.proto](../../types/types.md#metaproto)

**[Примеры](update/examples/update.md)**