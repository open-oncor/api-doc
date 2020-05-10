## Базовый сценарий работы внешней системы с API для ДЭЗО
1. ***Посредством пользовательского интерфейса*** ОНКОР создается запись [Заявка на ДЭЗО (Rc.RcTm66Order)](types/types.md#com.siams.med.api.Rc.RcTm66Order)  
1. [Поиск новых заявок на ДЭЗО с конкретной даты (или без нее) - по текущее время](methods/search/start/RcTm66OrderQuery/) `Получаем ID задачи` ([SearchJob.id](types/types.html#com.siams.med.api.SearchJob)) `используя который отдельным запросом, можно постранично получать данные`
2. [Постраничное получение заявок, найденных в запросе (п.2)](methods/search/get/RecordsPage/)
    `Запрос: page.job.id - ID задачи; page.offset - смещение от 0 объекта содержимого задачи; page.size - количество требумых объектов. Ответ: result.page.job.ready=false - задача еще не закончила обрабатывать запрос, необходимо повторить этот метод через некоторое время; result.size=X - фактическое количество объектов в задаче без учета page.offset`
3. [Получение информации о пациенте](methods/patient/get/)
4. [Установка статуса "Обработка началась"](methods/status/update/)
5. [Установка статуса "DICOM ассоциирован с заказом"](methods/status/update/)
6. Выполнение ДЭЗО
   1. [Отказ в проведении ДЭЗО](methods/tm66/order/addRcTm66OrderReject/)
   2. Сформировано заключение - `Сначала передается сформированный файл заключения и, по мере необходимости, файл открепленной ЭЦП к первому файлу. Полученные {{attachmentId}} файлов, используются в запросе передачи заключения`
       1. [Передача файла(-ов) заключения (файл протокола заключения и открепленно ЭЦП)](methods/attachment/create/index.md)
       2. [Передача заключения со ссылкой на ранее переданные файлы заключения](methods/tm66/order/addRcTm66OrderConclusion/index.md)
3. [Проведена экспертиза DICOM](methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) 
4. [Проведена экспертиза первичного протокола исследования](methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) 

---
## Методы API для ДЭЗО

### Получение документов ДЭЗО

* [/tm66/order/addRcTm66OrderReject](methods/tm66/order/addRcTm66OrderReject/index.md) - `загрузка документа "Отказ в проведении ДЭЗО"` 
* [/tm66/order/addRcTm66OrderConclusion](methods/tm66/order/addRcTm66OrderConclusion/index.md) - `загрузка документа "Заключение эксперта ДЭЗО"`
* [/tm66/order/addRcTm66OrderExpertiseDicom](methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) - `загрузка документа "Экспертиза качества DICOM"`
* [/tm66/order/addRcTm66OrderExpertiseProtocol](methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) - `загрузка документа "Экспертиза качества первичного протокола исследования"`

---

### Поисковые функции для медицинских записей

* [/search/start/RcTm66OrderQuery](methods/search/start/RcTm66OrderQuery/index.md)  - `поиск заявок на ДЭЗО`
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md)  - `постраничное получение найденных ранее в поисковом запросе записей`

---

### Работа со статусами записей

Работа со статусами записи *Заявки на ДЭЗО* ([Rc.RcTm66Order](types/types.md#com.siams.med.api.Rc.RcTm66Order)) в рамках ДЭЗО осуществляется приведенными ниже методами. Статус также обновляется при загрузке документов по этой заявке или по другим событиям
* [/rc/getInstanceStatus](methods/status/get/index.md)  - `получение статуса медицинской записи`
* [/rc/updateInstanceStatus](methods/status/update/index.md)  - `установка статуса медицинской записи`

---

### Работа со справочниками

* [/directory/get/Tm66OrderPurpose](methods/directory/get/Tm66OrderPurpose/index.md)  - `справочник Цель ДЭЗО` 
* [/directory/get/Tm66DiagnosticsType](methods/directory/get/Tm66DiagnosticsType/index.md)  - `справочник Тип диагностики ДЭЗО`
* [/directory/get/Tm66ConclusionType](methods/directory/get/Tm66ConclusionType/index.md)  - `справочник Тип заключения ДЭЗО`
* [/directory/get/Tm66OrderRejectReason](methods/directory/get/Tm66OrderRejectReason/index.md)  - `справочник Причины отказа проведения ДЭЗО`
* [/directory/get/Tm66ExpertProtocolResult](methods/directory/get/Tm66ExpertProtocolResult/index.md) - `cправочник типа значимости замечаний эксперта к к первичному протоколу исследования`  
* [/directory/get/Tm66ExpertDicomResult](methods/directory/get/Tm66ExpertDicomResult/index.md) - `cправочник типа значимости замечаний эксперта к DICOM `
* [/directory/get/MO](methods/directory/get/MO/index.md) - `cправочник медицинских организаций `  
* [/directory/get/MedDepart](methods/directory/get/MedDepart/index.md) - `cправочник подразделений медицинских организаций `  
* [/directory/get/MedResource](methods/directory/get/MedResource/index.md) - `cправочник врачей медицинских организаций `

### Работа с пациентами

* [/patient/get](methods/patient/get/index.md)  - `получение данных пациента по его ключу`


### Работа с медицинскими записями

* [/rc/get](methods/rc/get/index.md)  - `получение медицинской записи пациента по ключу`

