Работа с вложениями
===================

### ![GET](../../img/get.png) [/attachment/get`?id={id}`](get/index.md)
* **URL parameter:** [id](../../types/types.md#attachmentmeta)
* **Response:** [[Attachment](../../types/types.md#attachment)]

Возвращает объект типа [Attachment](../../types/types.md#attachment) с идентификатором [id](../../types/types.md#attachmentmeta)

[Examples](get/examples/get.md)

---

<a name="file"></a>

### ![GET](../../img/get.png) /attachment/file`?id={id}`
* **URL parameter:** [id](../../types/types.md#attachmentmeta)
* **Response:** [[File](../../types/types.md#attachment)]

Возвращает объект типа [File](../../types/types.md#attachment) с идентификатором [id](../../types/types.md#attachmentmeta)

---

### ![POST](../../img/post.png) [/attachment/create](create/index.md)
* **Request:** [Attachment](../../types/types.md#attachment) **attachment**
* **Response:** [[Attachment](../../types/types.md#attachment)]

Создаёт новое вложение. В запросе передаётся [Attachment](../../types/types.md#attachment). 

В ответе передаётся [Attachment](../../types/types.md#attachment).

[Examples](create/examples/create.md)

---

### ![POST](../../img/post.png) /attachment/query 
* **Request:** [Query](../../types/types.md#attachmentquery) query
* **Response:** [[Attachment](../../types/types.md#attachment)]

Возвращает список вложений В запросе передаётся массив [id](../../types/types.md#attachmentmeta).

В ответе передаётся массив [Attachment](../../types/types.md#attachment) c указанными [id](../../types/types.md#attachmentmeta).

**[Examples](query/examples/query.md)**