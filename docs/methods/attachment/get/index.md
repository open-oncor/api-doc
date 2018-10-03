[Работа с вложениями](../index.md)
=====================================

<a name="get"/>

### ![GET](../../../img/get.png) /attachment/get`?id={id}`
* **URL parameter:** [id](../../../types.md#attachmentmeta)
* **Response:** [[Attachment](../../../types.md#attachment)]

Возвращает объект типа [Attachment](../../../types.md#attachment) с идентификатором [id](../../../types.md#attachmentmeta)

Поле [Attachment.data](../../../types.md#attachment) представляет собой [ByteString](../../../types.md#scalar-value-types)

[Examples](examples/get.md)