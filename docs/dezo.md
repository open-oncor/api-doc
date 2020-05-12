## Методы API для ДЭЗО

1. [Сценарии работы внешней системы с API для ДЭЗО](#сценарий-работы-внешней-системы-с-api-для-дэзо)
   * [Базовый сценарий работы c записями](#базовый-сценарий-работы-c-записями)
   * [Сценарий работы с вложениями](#сценарий-работы-с-вложениями)
2. [Методы API](#методы-api)
   * [Получение документов ДЭЗО](#получение-документов-дэзо)
   * [Поисковые функции для медицинских записей](#поисковые-функции-для-медицинских-записей)
   * [Работа со статусами записей](#работа-со-статусами-записей)
   * [Работа со справочниками](#работа-со-справочниками)
   * [Работа с пациентами](#работа-с-пациентами)
   * [Работа с медицинскими записями](#работа-с-медицинскими-записями)
   * [Работа с вложениями к записям (attachment)](#работа-с-вложениями-к-записям)

---
## Сценарии работы внешней системы с API для ДЭЗО
### Базовый сценарий работы c записями
1. ***Посредством пользовательского интерфейса*** ОНКОР создается запись [Заявка на ДЭЗО (Rc.RcTm66Order)](types/types.md#com.siams.med.api.Rc.RcTm66Order)  
1. [Поиск новых заявок на ДЭЗО с конкретной даты (или без нее) - по текущее время](methods/search/start/RcTm66OrderQuery/index.md) `Получаем ID задачи` ([SearchJob.id](types/types.html#com.siams.med.api.SearchJob)) `используя который отдельным запросом, можно постранично получать данные`
2. [Постраничное получение заявок, найденных в запросе (п.2)](methods/search/get/RecordsPage/index.md)
    `Запрос: page.job.id - ID задачи; page.offset - смещение от 0 объекта содержимого задачи; page.size - количество требумых объектов. Ответ: result.page.job.ready=false - задача еще не закончила обрабатывать запрос, необходимо повторить этот метод через некоторое время; result.size=X - фактическое количество объектов в задаче без учета page.offset`
3. [Получение информации о пациенте](methods/patient/get/index.md)
4. [Установка статуса "Обработка началась"](methods/status/update/index.md)
5. [Установка статуса "DICOM ассоциирован с заказом"](methods/status/update/index.md)
6. Выполнение ДЭЗО
   1. [Отказ в проведении ДЭЗО](methods/tm66/order/addRcTm66OrderReject/index.md)
   2. Сформировано заключение - `Сначала передается сформированный файл заключения и, по мере необходимости, файл открепленной ЭЦП к первому файлу. Полученные {{attachmentId}} файлов, используются в запросе передачи заключения`
       1. [Передача файла(-ов) заключения (файл протокола заключения и открепленно ЭЦП)](methods/attachment/create/index.md)
       2. [Передача заключения со ссылкой на ранее переданные файлы заключения](methods/tm66/order/addRcTm66OrderConclusion/index.md)
3. [Проведена экспертиза DICOM](methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) 
4. [Проведена экспертиза первичного протокола исследования](methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) 

### Сценарий работы с вложениями
1. [Загрузка файла](methods/attachment/create//index.md) - `Загрузка файла для прикрепления к записи (документа) производится до момента непосредственного прикрепления`
2. Прикрепление файла к записи - `При использовании метода [attachment/create] получаем значение {attachment.id}, его указываем для прикрепления в других API-методах` 
3. Получение мета-информации о прикрепленных файлах
    * [/attachment/get](methods/attachment/get/index.md) - `получаем и мета-информацию и сами данные файла в формате Base64 в поле Attachment.data`
    * [/attachment/query](methods/attachment/query/index.md) - `получаем только мета-информацию о нескольких вложениях`
4. Получение файла
    * [/attachment/get](methods/attachment/get/index.md) - `получаем и мета-информацию о файле и сами данные файла`
    * [/attachment/file](methods/attachment/file/index.md) - `получаем сам файл`
5. Прямая ссылка на файл - `зная мета-информацию о файле можно сформировать прямую ссылку на файл вида /attachment/${digest}:${id}"`
```
    Attachment.id :     "#1587:4384" // символ # в итоговом адресе нужно удалить  
    Attachment.digest:  "6e4a3290ff2ab22fed4e747c95678bbf534b41d0"
    
    http://{{ONCOR-HOST}}/attachment/6e4a3290ff2ab22fed4e747c95678bbf534b41d0:1587:4384
```
    `Attachment.id - не предназначен для долговременного хранения во внешних системах, т.к. id может "устареть" и быть удален.`
---
## Методы API

### Получение документов ДЭЗО

* [/tm66/order/addRcTm66OrderReject](methods/tm66/order/addRcTm66OrderReject/index.md) - `загрузка документа "Отказ в проведении ДЭЗО"` 
* [/tm66/order/addRcTm66OrderConclusion](methods/tm66/order/addRcTm66OrderConclusion/index.md) - `загрузка документа "Заключение эксперта ДЭЗО"`
* [/tm66/order/addRcTm66OrderExpertiseDicom](methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) - `загрузка документа "Экспертиза качества DICOM"`
* [/tm66/order/addRcTm66OrderExpertiseProtocol](methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) - `загрузка документа "Экспертиза качества первичного протокола исследования"`

### Поисковые функции для медицинских записей

* [/search/start/RcTm66OrderQuery](methods/search/start/RcTm66OrderQuery/index.md)  - `поиск заявок на ДЭЗО`
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md)  - `постраничное получение найденных ранее в поисковом запросе записей`

### Работа со статусами записей

Работа со статусами записи *Заявки на ДЭЗО* ([Rc.RcTm66Order](types/types.md#com.siams.med.api.Rc.RcTm66Order)) в рамках ДЭЗО осуществляется приведенными ниже методами. Статус также обновляется при загрузке документов по этой заявке или по другим событиям
* [/rc/getInstanceStatus](methods/status/get/index.md)  - `получение статуса медицинской записи`
* [/rc/updateInstanceStatus](methods/status/update/index.md)  - `установка статуса медицинской записи`

### Работа со справочниками

* [/directory/get/Tm66OrderPurpose](methods/directory/get/Tm66OrderPurpose/index.md)  - `справочник Цель ДЭЗО` 
* [/directory/get/Tm66DiagnosticsType](methods/directory/get/Tm66DiagnosticsType/index.md)  - `справочник Тип диагностики ДЭЗО`
* [/directory/get/Tm66DiagnosticsMethod](methods/directory/get/Tm66DiagnosticsMethod/index.md)  - `справочник Тип инструментальной диагностики в первичном протоколе исследования`
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
* [/rc/link](methods/rc/link/index.md)  - `"прямая" ссылка на просмотр медицинской записи`

### Работа с вложениями к записям

* [/attachment/create](methods/attachment/create/index.md) - `загружаем новый файл`
* [/attachment/get](methods/attachment/get/index.md) - `получаем и мета-информацию и сам файл в формате ByteString в поле Attachment.data`
* [/attachment/query](methods/attachment/query/index.md) - `получаем только мета-информацию о нескольких файлах`
* [/attachment/file](methods/attachment/file/index.md) - `получаем сам файл`