##Полный перечень методов API

### Работа с пациентами
`Приём, изменение и выдача по поисковым запросам данных о лицах (пациентах), обращавшихся в медицинские организации региона за медицинской помощью по профилю 'онкология'`
* [GET/patient/search(new)](methods/patient/search/indexGET.md) ![info](img/info.png) -`поиск пациентов`
* [POST/patient/search(dated)](methods/patient/search/index.md) - `поиск пациентов`
* [/patient/get](methods/patient/get/index.md)  - `получение данных пациента по его ключу`
* [/patient/update](methods/patient/update/index.md)  - `изменение данных пациента` 
* [/patient/add](methods/patient/add/index.md)  - `добавление пациента`
* [/patient/forceAdd](methods/patient/forceAdd/index.md)  - `добавление пациента без анализа 'двойников'`

---

### Работа с заболеваниями пациента

`Приём, хранение и добавление данных о заболеваниях пациента. Заболеванием пациента является его предварительный или окончательно установленный диагноз. У пациента не может быть зарегистрировано два одинаковых диагноза. В процессе проведения диагностических исследований пациенту диагноз может быть подтвержден, изменен или отвергнут.`

* [/ehr/getList](methods/ehr/getList/index.md)  - `получение списка заболеваний пациента`
* [/ehr/add](methods/ehr/add/index.md)  - `регистрация заболевания пациента`
* [/ehr/record/add(RcDz)](methods/ehr/record/add/RcDz/index.md)  - `добавление диагноза в указанное заболевание` 

---

### Работа с медицинскими записями

`Приём, хранение и добавление медицинских записей пациента. Медицинские записи пациента могут находится на одном из двух уровней иерархии: привязаны непосредственно к данным пациента (записи общие для пациента) или привязаны к одному из заболеваний пациента. Записи условно можно разделить на статистические записи и медицинские документы. Статистические записи предназначены для формирования онкологической статистики. Медицинские документы формируют электронную историю болезни. При добавлении медицинских записей пациента необходимо соблюдать требования к их расположению в иерархии данных пациента.`

* [/rc/getList](methods/rc/getList/index.md)  - `получение списка медицинских записей пациента для указанного заболевания`
* [/patient/record/getList](methods/patient/record/getList/index.md)  - `получение списка медицинских записей общих для пациента (не привязанных к конкретному заболеванию)`
* [/rc/get](methods/rc/get/index.md)  - `получение медицинской записи пациента по ключу`
* [/ehr/record/add(RcReferral)](methods/ehr/record/add/RcReferral/index.md)  - `добавление направления в указанное заболевание`
* [/ehr/record/add(RcOper)](methods/ehr/record/add/RcOper/index.md)  - `добавление статистической записи 'Хирургическое лечение' в указанное заболевание`
* [/ehr/record/add(RcRay)](methods/ehr/record/add/RcRay/index.md)  - `добавление статистической записи 'Лучевая терапия' в указанное заболевание` 
* [/ehr/record/add(RcChem)](methods/ehr/record/add/RcChem/index.md)  - `добавление статистической записи 'Химиотерапия' в указанное заболевание` 
* [/ehr/record/add(RcHorm)](methods/ehr/record/add/RcHorm/index.md)  - `добавление статистической записи 'Гормонотерапия' в указанное заболевание` 
<!--- todo добавить описание как создать спецлечение? -->
* [/ehr/record/delete](methods/ehr/record/delete/index.md) - `удаление записи из указанного заболевания`
* [/patient/record/add(RcDoc)](methods/patient/record/add/index.md) - `добавление медицинской записи пациенту`
* [/patient/record/add(RcRegIn)](methods/patient/record/add/RcRegIn/index.md) - `добавление статистической записи 'Постановка на учёт' указанному пациенту`
* [/patient/record/add(RcRegOut)](methods/patient/record/add/RcRegOut/index.md) - `добавление статистической записи 'Снятие с учёта' указанному пациенту`
* [/patient/record/add(RcDeath)](methods/patient/record/add/RcDeath/index.md) - `добавление статистической записи 'Регистрация смерти' указанному пациенту`
* [/patient/record/add(RcClinicalGroup)](methods/patient/record/add/RcClinicalGroup/index.md) - `добавление статистической записи 'Установка клинической группы' указанному пациенту`
* [/patient/record/delete](methods/patient/record/delete/index.md) - `удаление записи указанного пациента`
* [/patient/RcReferralRl/getList](methods/patient/RcReferralRl/getList/index.md)  - `получение списка направлений пациента`
* [/patient/RcAppointment/add](methods/patient/RcAppointment/add/index.md)  - `добавление предварительной записи пациента на приём`

---

### Поисковые функции для медицинских записей

* [/search/start/RcReferralQuery](methods/search/start/RcReferralQuery/index.md)  - `поиск направлений по набору условий`
* [/search/start/RcAppointmentQuery](methods/search/start/RcAppointmentQuery/index.md)  - `поиск предварительных записей на приём для пациента по набору условий`
* [/search/start/RcDocQuery](methods/search/start/RcDocQuery/index.md)  - `поиск медицинских документов пациента`
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md)  - `постраничное получение найденных ранее в поисковом запросе записей`

---

### Работа с вложениями

`Приём, изменение и выдача вложений, присоединенных к другим записям о пациенте`

* [/attachment/query](methods/attachment/query/index.md)  - `получение списка вложений по набору их ключей`
* [/attachment/get](methods/attachment/get/index.md)  - `получение описания вложения`
* [/attachment/file](methods/attachment/file/index.md) ![info](img/info.png) - `получение содержимого вложения`
* [/attachment/create](methods/attachment/create/index.md)  - `добавление вложения`

---

### Работа с метаданными

`Приём, изменение и выдача метаданных, присоединенных к другим записям о пациенте`

* [/meta/query](methods/meta/query/index.md)  - `получение массива метаданных`
* [/meta/update](methods/meta/update/index.md)  - `изменение метаданных для медицинской записи`

---

### Работа со статусами записей

`Получение и установка статусов записей

* [/rc/getInstanceStatus](methods/status/get/index.md)  - `получение статуса медицинской записи`
* [/rc/updateInstanceStatus](methods/status/update/index.md)  - `установка статуса медицинской записи`

---

### Работа со справочниками

`Хранение и выдача содержимого справочников комплекса`
<!-- todo а МКБ-10? -->
<!-- todo а МКБ-О-2? -->

* [/directory/get/DrPrsG](methods/directory/get/DrPrsG/index.md)  - `справочник половой принадлежности` 
* [/directory/get/BloodType](methods/directory/get/BloodType/index.md)  - `справочник групп крови`
* [/directory/get/DiagnosticsType](methods/directory/get/DiagnosticsType/index.md) ![info](img/info.png) - `справочник диагностических исследований`
* [/directory/get/AddressType](methods/directory/get/AddressType/index.md)   - `справочник типов адресов`
* [/directory/get/MedOrgType](methods/directory/get/MedOrgType/index.md) ![info](img/info.png) - `справочник типов медицинских организаций`
* [/directory/get/DzStage](methods/directory/get/DzStage/index.md) ![info](img/info.png) - `справочник стадий`
* [/directory/get/TnmT](methods/directory/get/TnmT/index.md) ![info](img/info.png) - `справочник T`
* [/directory/get/TnmN](methods/directory/get/TnmN/index.md) ![info](img/info.png) - `справочник N`
* [/directory/get/TnmM](methods/directory/get/TnmM/index.md) ![info](img/info.png) - `справочник M`
* [/directory/get/TnmG](methods/directory/get/TnmG/index.md) ![info](img/info.png) - `справочник G`
* [/directory/get/DrDzHD](methods/directory/get/DrDzHD/index.md) ![info](img/info.png) - `справочник обстоятельств выявления заболевания`
* [/directory/get/DrNK0465](methods/directory/get/DrNK0465/index.md)  - `справочник операций`
* [/directory/get/DrNK0439](methods/directory/get/DrNK0439/index.md)  - `справочник осложнений`
* [/directory/get/TherapyCond](methods/directory/get/TherapyCond/index.md)  - `справочник условий проведения лечения`
* [/directory/get/LocMetType](methods/directory/get/LocMetType/index.md)  - `справочник типов отдаленных метастаз`
* [/directory/get/Srv59oper](methods/directory/get/Srv59oper/index.md)  - `справочник услуг при лечении онкологического заболевания (приказ ФФОМС от 30.03.2018 № 59)`
* [/medOrg/getList](methods/directory/medOrg/getList/index.md)  - `список медицинских организаций региона` 
* [/medTerr/getList](methods/directory/medTerr/getList/index.md) ![info](img/info.png) - `список территорий региона`
* [/locality/getList](methods/directory/locality/getList/index.md) ![info](img/info.png) - `список населённых пунктов региона`
* [/drug/getList](methods/directory/drug/getList/index.md) ![info](img/info.png) - `список препаратов`
* [/user/getList](methods/directory/user/getList/index.md)  - `список пользователей`
