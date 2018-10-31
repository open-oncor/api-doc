[Работа с вложениями](../index.md)
=====================================

<a name="get"/>

### ![GET](../../../img/get.png) /attachment/get`?id={id}`
* **URL parameter:** [id](../../../types/types.md#attachmentmeta)
* **Response:** [[Attachment](../../../types/types.md#com.siams.med.api.Attachment)]

Возвращает объект типа [Attachment](../../../types/types.md#com.siams.med.api.Attachment) с идентификатором [id](../../../types/types.md#attachmentmeta)

Поле [Attachment.data](../../../types/types.md#com.siams.med.api.Attachment) представляет собой [ByteString](../../../types/types.md#scalar-value-types)

**[HTTP примеры](examples/get.md)**
**[Java пример](examples/getJava.md)**