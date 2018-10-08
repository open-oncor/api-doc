### [Работа с пациентами](methods/patient/index.md)
`Модуль работы с пациентом обеспечивает прием, хранение, изменение и выдачу по поисковым запросам данных о лицах (пациентах), обращавшихся в медицинские организации региона за медицинской помощью по профилю "онкология"`

* [/patient/get](methods/patient/get/index.md) ![done](img/done.png)
* [/patient/add](methods/patient/add/index.md) ![done](img/done.png)
* [/patient/search](methods/patient/search/index.md) ![done](img/done.png)
* [/patient/forceAdd](methods/patient/forceAdd/index.md) ![done](img/done.png)
* [/patient/update](methods/patient/update/index.md) ![done](img/done.png)
* [/patient/record/add](methods/patient/index.md#add)
* [/patient/record/getList](methods/patient/record/getList/index.md) ![done](img/done.png)
* [/patient/RcAppointment/add](methods/patient/RcAppointment/add/index.md) ![done](img/done.png)
* [/patient/getList](methods/patient/index.md#getList)
* [/patient/RcReferralRl/getList](methods/patient/RcReferralRl/getList/index.md) ![done](img/done.png)

---

### [Работа со справочниками](methods/directory/index.md)

`Модуль работы со справочниками обеспечивает хранение и выдачу содержимого справочников комплекса`

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

---

### [Работа с заболеваниями пациента](methods/ehr/index.md)

`Получение, добавление данных о заболеваниях пациента`

* [/ehr/getList](methods/ehr/getList/index.md) ![done](img/done.png) - `получение списка заболеваний пациента`
* [/ehr/add](methods/ehr/add/index.md) ![done](img/done.png) - `регистрация нового заболевания пациента`
* [/ehr/record/add](methods/ehr/record/add/index.md) ![done](img/done.png) - `добавление медицинской записи в указанное заболевание` 
* [/ehr/getActive](methods/ehr/getActive/index.md) ![done](img/done.png) - `устаревший метод`

---

### [Работа с записями](methods/rc/index.md)

`Получение записей`

* [/rc/get](methods/rc/get/index.md) ![done](img/done.png)
* [/rc/getList](methods/rc/getList/index.md) ![done](img/done.png)

---

### [Работа с вложениями](methods/attachment/index.md)

`Модуль работы с вложенями обеспечивает прием, хранение, изменение и выдачу выложений, присоединенных к другим записям о пациенте`

* [/attachment/get](methods/attachment/get/index.md) ![done](img/done.png)
* [/attachment/file](methods/attachment/index.md#file)
* [/attachment/create](methods/attachment/create/index.md) ![done](img/done.png)
* [/attachment/query](methods/attachment/query/index.md) ![done](img/done.png)

---

### [Работа с метаданными](methods/meta/index.md)

`Получение метаданных`

* [/meta/query](methods/meta/query/index.md) ![done](img/done.png)
* [/meta/update](methods/meta/update/index.md) ![done](img/done.png)

---

### [Поисковые функции](methods/search/index.md)

`Поиск записей`

* [/search/start/RcReferralQuery](methods/search/start/RcReferralQuery/index.md) ![done](img/done.png)
* [/search/start/RcAppointmentQuery](methods/search/start/RcAppointmentQuery/index.md) ![done](img/done.png)
* [/search/start/RcDocQuery](methods/search/start/RcDocQuery/index.md) ![done](img/done.png)
* [/search/get/RecordsPage](methods/search/get/RecordsPage/index.md) ![done](img/done.png)
