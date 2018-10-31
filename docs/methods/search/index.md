Работа с поиском
================

### ![POST](../../img/post.png) [/search/start/RcReferralQuery](start/RcReferralQuery/index.md)
* **Request:** [RcReferralQuery](../../types/types.md#com.siams.med.api.RcReferralQuery) **query**
* **Response:** [[SearchJob](../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcReferralQuery](../../types/types.md#com.siams.med.api.RcReferralQuery).

В ответе передаётся [SearchJob](../../types/types.md#com.siams.med.api.SearchJob)

**[Примеры](start/RcReferralQuery/examples/RcReferralQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcAppointmentQuery](start/RcAppointmentQuery/index.md)
* **Request:** [RcAppointmentQuery](../../types/types.md#com.siams.med.api.RcAppointmentQuery) **query**
* **Response:** [[SearchJob](../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcAppointmentQuery](../../types/types.md#com.siams.med.api.RcAppointmentQuery). 

В ответе передаётся [SearchJob](../../types/types.md#com.siams.med.api.SearchJob)

**[Примеры](start/RcAppointmentQuery/examples/RcAppointmentQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcDocQuery](start/RcDocQuery/index.md)
* **Request:** [RcDocQuery](../../types/types.md#com.siams.med.api.RcDocQuery) **query**
* **Response:** [[SearchJob](../../types/types.md#com.siams.med.api.SearchJob)]

В запросе передаётся [RcDocQuery](../../types/types.md#com.siams.med.api.RcDocQuery). 
В ответе передаётся [SearchJob](../../types/types.md#com.siams.med.api.SearchJob)

**[Примеры](start/RcDocQuery/examples/RcDocQuery.md)**

---

### ![POST](../../img/post.png) [/search/get/RecordsPage](get/RecordsPage/index.md)
* **Request:** [Page](../../types/types.md#com.siams.med.api.Page) **page** <job>
* **Response:** [[RecordsPage](../../types/types.md#com.siams.med.api.RecordsPage)]

Постранично ищет записи. 

В запрос передаётся 

[Page](../../types/types.md#com.siams.med.api.Page)
* required [job](../../types/types.md#com.siams.med.api.SearchJob)

В ответ переаётся [RecordsPage](../../types/types.md#com.siams.med.api.RecordsPage).

**[Примеры](get/RecordsPage/examples/RecordsPage.md)**