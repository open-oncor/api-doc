[Работа с вложениями](../index.md)
=====================================

<a name="create"/>

### ![POST](../../../img/post.png) /attachment/create
* **Request:** [Attachment](../../../types/types.md#attachment) **attachment**
* **Response:** [[Attachment](../../../types/types.md#attachment)]

Создаёт новое вложение. 

В запросе передаётся [Attachment](../../../types/types.md#attachment). 

В ответе передаётся [Attachment](../../../types/types.md#attachment).

Поле [Attachment.data](../../../types/types.md#attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

**[Примеры](examples/create.md)**