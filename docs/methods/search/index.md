Работа с поиском
================

### ![POST](../../img/post.png) [/search/start/RcReferralQuery](start/RcReferralQuery/index.md)
* **Request:** [RcReferralQuery](../../types/types.md#rcreferralquery) **query**
* **Response:** [[SearchJob](../../types/types.md#searchjob)]

В запросе передаётся [RcReferralQuery](../../types/types.md#rcreferralquery).

В ответе передаётся [SearchJob](../../types/types.md#searchjob)

**[Примеры](start/RcReferralQuery/examples/RcReferralQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcAppointmentQuery](start/RcAppointmentQuery/index.md)
* **Request:** [RcAppointmentQuery](../../types/types.md#rcappointmentquery) **query**
* **Response:** [[SearchJob](../../types/types.md#searchjob)]

В запросе передаётся [RcAppointmentQuery](../../types/types.md#rcappointmentquery). 

В ответе передаётся [SearchJob](../../types/types.md#searchjob)

**[Примеры](start/RcAppointmentQuery/examples/RcAppointmentQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcDocQuery](start/RcDocQuery/index.md)
* **Request:** [RcDocQuery](../../types/types.md#rcdocquery) **query**
* **Response:** [[SearchJob](../../types/types.md#searchjob)]

В запросе передаётся [RcDocQuery](../../types/types.md#rcdocquery). 
В ответе передаётся [SearchJob](../../types/types.md#searchjob)

**[Примеры](start/RcDocQuery/examples/RcDocQuery.md)**

---

### ![POST](../../img/post.png) [/search/get/RecordsPage](get/RecordsPage/index.md)
* **Request:** [Page](../../types/types.md#page) **page** <job>
* **Response:** [[RecordsPage](../../types/types.md#recordspage)]

Постранично ищет записи. 

В запрос передаётся 

[Page](../../types/types.md#page)
* required [job](../../types/types.md#searchjob)

В ответ переаётся [RecordsPage](../../types/types.md#recordspage).

**[Примеры](get/RecordsPage/examples/RecordsPage.md)**