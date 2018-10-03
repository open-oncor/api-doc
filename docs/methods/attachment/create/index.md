[Работа с вложениями](../index.md)
=====================================

<a name="create"/>

### ![POST](../../../img/post.png) /attachment/create
* **Request:** [Attachment](../../../types.md#attachment) **attachment**
* **Response:** [[Attachment](../../../types.md#attachment)]

Создаёт новое вложение. 

В запросе передаётся [Attachment](../../../types.md#attachment). 

В ответе передаётся [Attachment](../../../types.md#attachment).

Поле [Attachment.data](../../../types.md#attachment) представляет собой [ByteString](../../../types.md#scalar-value-types)

[Examples](examples/create.md)