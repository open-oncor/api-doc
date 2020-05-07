## Базовый сценарий работы внешней системы с API для ДЭЗО

1. [Поиск новых заявок на ДЭЗО](https://open-oncor.github.io/api-doc/methods/search/start/RcTm66OrderQuery/) с конкретной даты (или без нее) - по текущее время
2. [Постраничное получение заявок](https://open-oncor.github.io/api-doc/methods/search/get/RecordsPage/), найденных в запросе (п.1)
3. [Получение информации о пациенте](https://open-oncor.github.io/api-doc/methods/patient/get/)
4. [Установка статуса](https://open-oncor.github.io/api-doc/methods/status/update/) "Обработка началась"

## Методы API для ДЭЗО
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

