[Работа с вложениями](../index.md)
=====================================

<a name="get"/>

### ![GET](../../../img/get.png) /attachment/get`?id={id}`
* **URL parameter:** [id](../../../types/types.md#attachmentmeta)
* **Response:** [[Attachment](../../../types/types.md#attachment)]

Возвращает объект типа [Attachment](../../../types/types.md#attachment) с идентификатором [id](../../../types/types.md#attachmentmeta)

Поле [Attachment.data](../../../types/types.md#attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

**[HTTP примеры](examples/get.md)**
**[Примеры кода](examples/getCode.md)**