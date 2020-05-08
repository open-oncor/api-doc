## Базовый сценарий работы внешней системы с API для ДЭЗО
1. ***Посредством пользовательского интерфейса*** ОНКОР создается запись *Заявка на ДЭЗО* - [Rc.RcTm66Order](../../types/types.md#com.siams.med.api.Rc.RcTm66Order)  
1. [Поиск новых заявок на ДЭЗО](https://open-oncor.github.io/api-doc/methods/search/start/RcTm66OrderQuery/) с конкретной даты (или без нее) - по текущее время
2. [Постраничное получение заявок](https://open-oncor.github.io/api-doc/methods/search/get/RecordsPage/), найденных в запросе (п.1)
3. [Получение информации о пациенте](https://open-oncor.github.io/api-doc/methods/patient/get/)
4. [Установка статуса](https://open-oncor.github.io/api-doc/methods/status/update/) "Обработка началась"
5. [Установка статуса](https://open-oncor.github.io/api-doc/methods/status/update/) "DICOM ассоциирован с заказом"
6. Выполнение ДЭЗО
   1. [Отказ в проведении ДЭЗО](https://open-oncor.github.io/api-doc/methods/tm66/order/addRcTm66OrderReject/)
   2. Сформировано заключение - `Сначала передается сформированный файл заключения и, по мере необходимости, файл открепленной ЭЦП к первому файлу. Полученные {{attachmentId}} файлов, изспользуются в запросе передачи заключения`
       1. [Передача файла(-ов)](https://open-oncor.github.io/api-doc/methods/attachment/create/index.md) заключения (например, PDF)
       2. [Передача заключения](https://open-oncor.github.io/api-doc/methods/tm66/order/addRcTm66OrderConclusion/index.md) со ссылкой на ранее переданные файлы заключения
3. [Проведена экспертиза DICOM](https://open-oncor.github.io/api-doc/methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) 
4. [Проведена экспертиза первичного протокола исследования](https://open-oncor.github.io/api-doc/methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) 

---
## Методы API для ДЭЗО

### Получение документов ДЭЗО
* [/tm66/order/addRcTm66OrderReject](methods/tm66/order/addRcTm66OrderReject/index.md) - `получение документа "Отказ в проведении ДЭЗО"` 
* [/tm66/order/addRcTm66OrderConclusion](methods/tm66/order/addRcTm66OrderConclusion/index.md) - `получение документа "Заключение эксперта ДЭЗО"`
* [/tm66/order/addRcTm66OrderExpertiseDicom](methods/tm66/tm66/order/addRcTm66OrderExpertiseDicom/index.md) - `получение документа "Экспертиза качества DICOM"`
* [/tm66/order/addRcTm66OrderExpertiseProtocol](methods/tm66/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) - `получение документа "Экспертиза качества первичного протокола исследования"`
---
### Поисковые функции для медицинских записей

* [/search/start/RcTm66OrderQuery](methods/search/start/RcTm66OrderQuery/index.md)  - `поиск заявок на ДЭЗО`
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md)  - `постраничное получение найденных ранее в поисковом запросе записей`

---

### Работа со статусами записей

* [/rc/getInstanceStatus](methods/status/get/index.md)  - `получение статуса медицинской записи`
* [/rc/updateInstanceStatus](methods/status/update/index.md)  - `установка статуса медицинской записи`

---

### Работа со справочниками

* [/directory/get/Tm66OrderPurpose](methods/directory/get/Tm66OrderPurpose/index.md)  - `справочник Цель ДЭЗО` 
* [/directory/get/Tm66DiagnosticsType](methods/directory/get/Tm66DiagnosticsType/index.md)  - `справочник Тип диагностики ДЭЗО`
* [/directory/get/Tm66ConclusionType](methods/directory/get/Tm66ConclusionType/index.md)  - `справочник Тип заключения ДЭЗО`
* [/directory/get/Tm66OrderRejectReason](methods/directory/get/Tm66OrderRejectReason/index.md)  - `справочник Причины отказа проведения ДЭЗО`


### Работа с пациентами
* [/patient/get](methods/patient/get/index.md)  - `получение данных пациента по его ключу`


### Работа с медицинскими записями

* [/rc/get](methods/rc/get/index.md)  - `получение медицинской записи пациента по ключу`

