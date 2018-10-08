### [Работа с пациентами](methods/patient/index.md)
`Приём, изменение и выдача по поисковым запросам данных о лицах (пациентах), обращавшихся в медицинские организации региона за медицинской помощью по профилю 'онкология'`

* [/patient/search](methods/patient/search/index.md) ![done](img/done.png) - `поиск пациентов`
* [/patient/get](methods/patient/get/index.md) ![done](img/done.png) - `получение данных пациента по его ключу`
* [/patient/update](methods/patient/update/index.md) ![done](img/done.png) - `изменение данных пациента` 
* [/patient/add](methods/patient/add/index.md) ![done](img/done.png) - `добавление пациента`
* [/patient/forceAdd](methods/patient/forceAdd/index.md) ![done](img/done.png) - `добавление пациента без анализа 'двойников'`

---

### [Работа с заболеваниями пациента](methods/ehr/index.md)

`Приём, хранение и добавление данных о заболеваниях пациента. Заболеванием пациента является его предварительный или окончательно установленный диагноз. У пациента не может быть зарегистрировано два одинаковых диагноза. В процессе проведения диагностических исследований пациенту диагноз может быть подтвержден, изменен или отвергнут.`

* [/ehr/getList](methods/ehr/getList/index.md) ![done](img/done.png) - `получение списка заболеваний пациента`
* [/ehr/add](methods/ehr/add/index.md) ![done](img/done.png) - `регистрация нового заболевания пациента`
* [/ehr/record/add](methods/ehr/record/add/index.md) ![done](img/done.png) - `добавление медицинской записи в указанное заболевание` 
* [/ehr/getActive](methods/ehr/getActive/index.md) ![done](img/done.png) - `устаревший метод`

---

### [Работа с медицинскими записями](methods/rc/index.md)

`Приём, хранение и добавление медицинских записей пациента. Медицинские записи пациента могут находится на одном из двух уровней иерархии: привязаны непссредственно к данным пациента (записи общие для пациента) или привязаны к одному из заболеваний пациента. Записи условно можно разделить на учётные записи и медицинские документы. Учётные записи предназначены для формировния онкологической статистики. Медицинские документы формируют электронную историю болезни. При добавлении медицинских записей пациента необходимо соблюдать требования к их расположению в иерархии данных пациента.`

* [/rc/getList](methods/rc/getList/index.md) ![done](img/done.png) - `получение списка медицинских записей пациента для указанного заболевания`
* [/patient/record/getList](methods/patient/record/getList/index.md) ![done](img/done.png) - `получение списка медицинских записей на всех уровнях (во всех заболеваниях, а также записей общих для пациента)`
* [/rc/get](methods/rc/get/index.md) ![done](img/done.png) - `получение медицинской записи пациента по ключу`
* [/patient/record/add](methods/patient/index.md) - `добавление медицинской записи пациенту`
* [/patient/RcReferralRl/getList](methods/patient/RcReferralRl/getList/index.md) ![done](img/done.png) - `добавление направления пациенту по его заболеванию`
* [/patient/RcAppointment/add](methods/patient/RcAppointment/add/index.md) ![done](img/done.png) - `добавление предварительной записи пациента на приём`

---

### [Поисковые функции для медицинских записей](methods/search/index.md)

* [/search/start/RcReferralQuery](methods/search/start/RcReferralQuery/index.md) ![done](img/done.png) - `поиск направлений по набору условий`
* [/search/start/RcAppointmentQuery](methods/search/start/RcAppointmentQuery/index.md) ![done](img/done.png) - `поиск предварительных записей на приём для пациента по набору условий`
* [/search/start/RcDocQuery](methods/search/start/RcDocQuery/index.md) ![done](img/done.png) - `поиск медицинских документов пациента`
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md) ![done](img/done.png) - `постраниченое получение найденных ранее в поисковом запросе записей`

---

### [Работа с вложениями](methods/attachment/index.md)

`Приём, изменение и выдача вложений, присоединенных к другим записям о пациенте`

* [/attachment/query](methods/attachment/query/index.md) ![done](img/done.png) - `получение списка вложений по набору их ключей`
* [/attachment/get](methods/attachment/get/index.md) ![done](img/done.png) - `получение описания вложения`
* [/attachment/file](methods/attachment/index.md) - `получение содержимого вложения`
* [/attachment/create](methods/attachment/create/index.md) ![done](img/done.png) - `добавление вложения`

---

### [Работа с метаданными](methods/meta/index.md)

`Приём, изменение и выдача метаданных, присоединенных к другим записям о пациенте`

* [/meta/query](methods/meta/query/index.md) ![done](img/done.png) - `получение массива метаданных`
* [/meta/update](methods/meta/update/index.md) ![done](img/done.png) - `изменение метаданных для медицинской записи`

---

### [Работа со справочниками](methods/directory/index.md)

`Хранение и выдачу содержимого справочников комплекса`

* [/directory/get/DrPrsG](methods/directory/get/DrPrsG/index.md) ![done](img/done.png) - `справочник половой принадлежности` 
* [/directory/get/BloodType](methods/directory/get/BloodType/index.md) ![done](img/done.png) - `справочник групп крови`
* [/directory/get/DiagnosticsType](methods/directory/get/DiagnosticsType/index.md) - `справочник диагностических исследований`
* [/directory/get/AddressType](methods/directory/get/AddressType/index.md)  ![done](img/done.png) - `справочник типов адресов`
* [/directory/get/MedOrgType](methods/directory/get/MedOrgType/index.md) - `справочник типов медицинских организаций`
* [/directory/get/DzStage](methods/directory/get/DzStage/index.md) - `справочник стадий`
* [/directory/get/TnmT](methods/directory/get/TnmT/index.md) - `справочник T`
* [/directory/get/TnmN](methods/directory/get/TnmN/index.md) - `справочник N`
* [/directory/get/TnmM](methods/directory/get/TnmM/index.md) - `справочник M`
* [/directory/get/TnmG](methods/directory/get/TnmG/index.md) - `справочник G`
* [/directory/get/DrDzHD](methods/directory/get/DrDzHD/index.md) - `справочник обстоятельств выявления заболевания`
* [/directory/get/DrNK0465](methods/directory/get/DrNK0465/index.md) ![done](img/done.png) - `справочник операций`
* [/directory/get/DrNK0439](methods/directory/get/DrNK0439/index.md) ![done](img/done.png) - `справочник осложнений`
* [/directory/get/TherapyCond](methods/directory/get/TherapyCond/index.md) ![done](img/done.png) - `справочник условий проведения лечения`
* [/directory/get/LocMetType](methods/directory/get/LocMetType/index.md) ![done](img/done.png) - `справочник типов отдаленных метастаз`
* [/directory/get/Srv59oper](methods/directory/get/Srv59oper/index.md) ![done](img/done.png) - `справочник услуг при лечении онкологического заболевания (приказ ФФОМС от 30.03.2018 № 59)`
* [/medOrg/getList](methods/directory/medOrg/getList/index.md) ![done](img/done.png) - `получение списка медицинских орагнизаций региона` 
* [/medTerr/getList](methods/directory/medTerr/getList/index.md) - `получение списка территорий региона`
* [/user/getList](methods/directory/user/getList/index.md) ![done](img/done.png) - `получение списка пользователей`
