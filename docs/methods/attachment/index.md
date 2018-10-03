Работа с вложениями
===================

### ![GET](../../img/get.png) [/attachment/get`?id={id}`](get/index.md)
* **URL parameter:** [id](../../types.md#attachmentmeta)
* **Response:** [[Attachment](../../types.md#attachment)]

Возвращает объект типа [Attachment](../../types.md#attachment) с идентификатором [id](../../types.md#attachmentmeta)

[Examples](get/examples/get.md)

---

### ![GET](../../img/get.png) /attachment/file`?id={id}`
* **URL parameter:** [id](../../types.md#attachmentmeta)
* **Response:** [[File](../../types.md#attachment)]

Возвращает объект типа [File](../../types.md#attachment) с идентификатором [id](../../types.md#attachmentmeta)

---

<a name="create"></a>

### ![POST](../../img/post.png) [/attachment/create](create/index.md)
* **Request:** [Attachment](../../types.md#attachment) **attachment**
* **Response:** [[Attachment](../../types.md#attachment)]

Создаёт новое вложение. В запросе передаётся [Attachment](../../types.md#attachment). 

В ответе передаётся [Attachment](../../types.md#attachment).

[Examples](create/examples/create.md)

---

<a name="query"></a>

### ![POST](../../img/post.png) /attachment/query 
* **Request:** [id](../../types.md#attachment)
* **Response:** [[Attachment](../../types.md#attachment)]

Возвращает список вложений В запросе передаётся массив [id](../../types.md#attachmentmeta).

В ответе передаётся массив [Attachment](../../types.md#attachment) c указанными [id](../../types.md#attachmentmeta).
