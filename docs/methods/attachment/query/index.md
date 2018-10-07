[Работа с вложениями](../index.md)
==================================

### ![POST](../../../img/post.png) /attachment/query 
* **Request:** [Query](../../../types/types.md#attachmentquery) query
* **Response:** [[Attachment](../../../types/types.md#attachment)]

Возвращает список вложений В запросе передаётся массив [id](../../../types/types.md#attachmentmeta).

В ответе передаётся массив [Attachment](../../../types/types.md#attachment) c указанными [id](../../../types/types.md#attachmentmeta).

**[HTTP примеры](examples/query.md)**
**[Примеры кода](examples/queryAttachment.md)**