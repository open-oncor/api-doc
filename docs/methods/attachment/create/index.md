[Работа с вложениями](../index.md)
=====================================

<a name="create"/>

### ![POST](../../../img/post.png) /attachment/create
* **Request:** [Attachment](../../../types/types.md#com.siams.med.api.Attachment) **attachment**
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Создаёт новое вложение. 

В запросе передаётся [Attachment](../../../types/types.md#com.siams.med.api.Attachment). 

В ответе передаётся [Attachment](../../../types/types.md#com.siams.med.api.Attachment).

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

**[Примеры](examples/create.md)**