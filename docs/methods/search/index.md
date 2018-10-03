Работа с поиском
================

### ![POST](../../img/post.png) [/search/start/RcReferralQuery](start/RcReferralQuery/index.md)
* **Request:** [RcReferralQuery](../../types.md#rcreferralquery) **query**
* **Response:** [[SearchJob](../../types.md#searchjob)]

В запросе передаётся [RcReferralQuery](../../types.md#rcreferralquery).

В ответе передаётся [SearchJob](../../types.md#searchjob)

**[Examples](start/RcReferralQuery/examples/RcReferralQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcAppointmentQuery](start/RcAppointmentQuery/index.md)
* **Request:** [RcAppointmentQuery](../../types.md#rcappointmentquery) **query**
* **Response:** [[SearchJob](../../types.md#searchjob)]

В запросе передаётся [RcAppointmentQuery](../../types.md#rcappointmentquery). 

В ответе передаётся [SearchJob](../../types.md#searchjob)

**[Examples](start/RcAppointmentQuery/examples/RcAppointmentQuery.md)**

---

### ![POST](../../img/post.png) [/search/start/RcDocQuery](start/RcDocQuery/index.md)
* **Request:** [RcDocQuery](../../types.md#rcdocquery) **query**
* **Response:** [[SearchJob](../../types.md#searchjob)]

В запросе передаётся [RcDocQuery](../../types.md#rcdocquery). 
В ответе передаётся [SearchJob](../../types.md#searchjob)

**[Examples](start/RcDocQuery/examples/RcDocQuery.md)**

---

### ![POST](../../img/post.png) [/search/get/RecordsPage](get/RecordsPage/index.md)
* **Request:** [Page](../../types.md#page) **page** <job>
* **Response:** [[RecordsPage](../../types.md#recordspage)]

Постранично ищет записи. 

В запрос передаётся 

[Page](../../types.md#page)
* required [job](../../types.md#searchjob)

В ответ переаётся [RecordsPage](../../types.md#recordspage).

**[Examples](get/RecordsPage/examples/RecordsPage.md)**