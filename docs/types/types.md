# Protocol Documentation
<a name="top"/>

## Table of Contents

- [api.proto](#api.proto)
    - [ErrorResult](#com.siams.med.api.ErrorResult)
    - [Response](#com.siams.med.api.Response)
    - [SuccessResult](#com.siams.med.api.SuccessResult)
  
  
  
  

- [attachments.proto](#attachments.proto)
    - [Attachment](#com.siams.med.api.Attachment)
    - [Attachment.Meta](#com.siams.med.api.Attachment.Meta)
    - [Attachment.Query](#com.siams.med.api.Attachment.Query)
  
  
  
  

- [diagnosis.proto](#diagnosis.proto)
    - [Dz](#com.siams.med.api.Dz)
    - [LocMet](#com.siams.med.api.LocMet)
    - [ShortDz](#com.siams.med.api.ShortDz)
    - [TNM](#com.siams.med.api.TNM)
  
  
  
  

- [directories.proto](#directories.proto)
    - [AddressType](#com.siams.med.api.AddressType)
    - [BloodType](#com.siams.med.api.BloodType)
    - [ChemKind](#com.siams.med.api.ChemKind)
    - [ClinicalGroupType](#com.siams.med.api.ClinicalGroupType)
    - [DiagnosticsType](#com.siams.med.api.DiagnosticsType)
    - [DoseUnit](#com.siams.med.api.DoseUnit)
    - [DrAutopsy](#com.siams.med.api.DrAutopsy)
    - [DrDzHD](#com.siams.med.api.DrDzHD)
    - [DrDzMthd](#com.siams.med.api.DrDzMthd)
    - [DrDzPl](#com.siams.med.api.DrDzPl)
    - [DrDzPr](#com.siams.med.api.DrDzPr)
    - [DrDzRA](#com.siams.med.api.DrDzRA)
    - [DrDzSt](#com.siams.med.api.DrDzSt)
    - [DrDzTM](#com.siams.med.api.DrDzTM)
    - [DrDzTS](#com.siams.med.api.DrDzTS)
    - [DrDzWO](#com.siams.med.api.DrDzWO)
    - [DrNK0439](#com.siams.med.api.DrNK0439)
    - [DrNK0465](#com.siams.med.api.DrNK0465)
    - [DrPrsG](#com.siams.med.api.DrPrsG)
    - [DrugType](#com.siams.med.api.DrugType)
    - [DzStage](#com.siams.med.api.DzStage)
    - [LocMetType](#com.siams.med.api.LocMetType)
    - [RBiFRV442](#com.siams.med.api.RBiFRV442)
    - [RBiMKB308](#com.siams.med.api.RBiMKB308)
    - [RBiNK0366](#com.siams.med.api.RBiNK0366)
    - [RBiPRK438](#com.siams.med.api.RBiPRK438)
    - [RBiPRP365](#com.siams.med.api.RBiPRP365)
    - [RayKind](#com.siams.med.api.RayKind)
    - [RayMethod](#com.siams.med.api.RayMethod)
    - [RayRadio](#com.siams.med.api.RayRadio)
    - [RayWay](#com.siams.med.api.RayWay)
    - [RegInClause](#com.siams.med.api.RegInClause)
    - [RegOutReason](#com.siams.med.api.RegOutReason)
    - [Srv59Chem](#com.siams.med.api.Srv59Chem)
    - [Srv59Oper](#com.siams.med.api.Srv59Oper)
    - [Srv59Ray](#com.siams.med.api.Srv59Ray)
    - [TherapyAim](#com.siams.med.api.TherapyAim)
    - [TherapyCond](#com.siams.med.api.TherapyCond)
    - [TnmG](#com.siams.med.api.TnmG)
    - [TnmM](#com.siams.med.api.TnmM)
    - [TnmN](#com.siams.med.api.TnmN)
    - [TnmT](#com.siams.med.api.TnmT)
  
    - [LocMetType.Code](#com.siams.med.api.LocMetType.Code)
  
  
  

- [meta.proto](#meta.proto)
    - [Object](#com.siams.med.api.Object)
    - [Object.Entry](#com.siams.med.api.Object.Entry)
    - [Query](#com.siams.med.api.Query)
    - [Update](#com.siams.med.api.Update)
    - [Update.Statment](#com.siams.med.api.Update.Statment)
  
    - [Update.Action](#com.siams.med.api.Update.Action)
  
  
  

- [oncor.proto](#oncor.proto)
    - [Locality](#com.siams.med.api.Locality)
    - [MedOrg](#com.siams.med.api.MedOrg)
    - [MedTerr](#com.siams.med.api.MedTerr)
    - [User](#com.siams.med.api.User)
  
  
  
  

- [patients.proto](#patients.proto)
    - [Address](#com.siams.med.api.Address)
    - [EHR](#com.siams.med.api.EHR)
    - [Insurance](#com.siams.med.api.Insurance)
    - [Patient](#com.siams.med.api.Patient)
    - [PatientQuery](#com.siams.med.api.PatientQuery)
    - [PatientSearchResult](#com.siams.med.api.PatientSearchResult)
    - [PatientUpdate](#com.siams.med.api.PatientUpdate)
    - [PatientUpdate.Entry](#com.siams.med.api.PatientUpdate.Entry)
  
  
  
  

- [records.proto](#records.proto)
    - [Drug](#com.siams.med.api.Drug)
    - [DrugRecord](#com.siams.med.api.DrugRecord)
    - [Rc](#com.siams.med.api.Rc)
    - [Rc.Published](#com.siams.med.api.Rc.Published)
    - [Rc.RcAppointment](#com.siams.med.api.Rc.RcAppointment)
    - [Rc.RcChem](#com.siams.med.api.Rc.RcChem)
    - [Rc.RcClinicalGroup](#com.siams.med.api.Rc.RcClinicalGroup)
    - [Rc.RcDeath](#com.siams.med.api.Rc.RcDeath)
    - [Rc.RcDoc](#com.siams.med.api.Rc.RcDoc)
    - [Rc.RcDz](#com.siams.med.api.Rc.RcDz)
    - [Rc.RcHorm](#com.siams.med.api.Rc.RcHorm)
    - [Rc.RcOper](#com.siams.med.api.Rc.RcOper)
    - [Rc.RcRay](#com.siams.med.api.Rc.RcRay)
    - [Rc.RcReferral](#com.siams.med.api.Rc.RcReferral)
    - [Rc.RcRegIn](#com.siams.med.api.Rc.RcRegIn)
    - [Rc.RcRegOut](#com.siams.med.api.Rc.RcRegOut)
  
  
  
  

- [routing.proto](#routing.proto)
    - [RoutingList](#com.siams.med.api.RoutingList)
    - [RoutingList.Diagnostics](#com.siams.med.api.RoutingList.Diagnostics)
  
  
  
  

- [search.proto](#search.proto)
    - [Page](#com.siams.med.api.Page)
    - [RcAppointmentQuery](#com.siams.med.api.RcAppointmentQuery)
    - [RcDocQuery](#com.siams.med.api.RcDocQuery)
    - [RcReferralQuery](#com.siams.med.api.RcReferralQuery)
    - [RecordsPage](#com.siams.med.api.RecordsPage)
    - [SearchJob](#com.siams.med.api.SearchJob)
  
  
  
  

- [Scalar Value Types](#scalar-value-types)



<a name="api.proto"/>
<p align="right"><a href="#top">Top</a></p>

## api.proto



<a name="com.siams.med.api.ErrorResult"/>

### ErrorResult



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) | required |  |
| message | [string](#string) | optional |  |
| uuid | [string](#string) | optional |  |






<a name="com.siams.med.api.Response"/>

### Response



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| success | [SuccessResult](#com.siams.med.api.SuccessResult) | optional |  |
| error | [ErrorResult](#com.siams.med.api.ErrorResult) | optional |  |






<a name="com.siams.med.api.SuccessResult"/>

### SuccessResult






 

 

 

 



<a name="attachments.proto"/>
<p align="right"><a href="#top">Top</a></p>

## attachments.proto



<a name="com.siams.med.api.Attachment"/>

### Attachment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| meta | [Attachment.Meta](#com.siams.med.api.Attachment.Meta) | required |  |
| data | [bytes](#bytes) | required |  |






<a name="com.siams.med.api.Attachment.Meta"/>

### Attachment.Meta



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| digest | [string](#string) | optional |  |
| name | [string](#string) | required |  |
| type | [string](#string) | required |  |
| size | [int64](#int64) | optional |  |
| created | [string](#string) | optional |  |






<a name="com.siams.med.api.Attachment.Query"/>

### Attachment.Query



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ids | [string](#string) | repeated |  |





 

 

 

 



<a name="diagnosis.proto"/>
<p align="right"><a href="#top">Top</a></p>

## diagnosis.proto



<a name="com.siams.med.api.Dz"/>

### Dz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| summary | [string](#string) | optional | Примечание |
| icd10 | [RBiMKB308](#com.siams.med.api.RBiMKB308) | optional | МКБ10 |
| status | [DrDzSt](#com.siams.med.api.DrDzSt) | optional | Тип диагноза |
| primacy | [DrDzPr](#com.siams.med.api.DrDzPr) | optional | Первичность установки диагноза |
| morph_class | [RBiNK0366](#com.siams.med.api.RBiNK0366) | optional | Морфологический тип |
| tumor_main | [DrDzTM](#com.siams.med.api.DrDzTM) | optional | Признак основной опухоли |
| tumor_side | [DrDzTS](#com.siams.med.api.DrDzTS) | optional | Сторона поражения |
| how_discover | [DrDzHD](#com.siams.med.api.DrDzHD) | optional | Обстоятельства выявления |
| method | [DrDzMthd](#com.siams.med.api.DrDzMthd) | optional | Метод подтверждения диагноза |
| plural | [DrDzPl](#com.siams.med.api.DrDzPl) | optional | Наличие первично-множественной опухоли |
| res_autopsy | [DrDzRA](#com.siams.med.api.DrDzRA) | optional | Результат аутопсии |
| why_old | [DrDzWO](#com.siams.med.api.DrDzWO) | optional | Причина поздней диагностики |
| loc_met | [LocMet](#com.siams.med.api.LocMet) | optional | Локализация отдаленных метастазов |
| tnm | [TNM](#com.siams.med.api.TNM) | optional | TNM |
| stage | [DzStage](#com.siams.med.api.DzStage) | optional | Стадия опухолевого процесса |






<a name="com.siams.med.api.LocMet"/>

### LocMet

Локализация отдаленных метастазов


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| codes | [LocMetType.Code](#com.siams.med.api.LocMetType.Code) | repeated |  |






<a name="com.siams.med.api.ShortDz"/>

### ShortDz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| summary | [string](#string) | optional |  |
| mkb_code | [string](#string) | optional |  |
| mkb_name | [string](#string) | optional |  |
| dz_date | [string](#string) | optional |  |
| tnm | [TNM](#com.siams.med.api.TNM) | optional |  |
| dz_stage | [DzStage](#com.siams.med.api.DzStage) | optional |  |
| how_discover | [DrDzHD](#com.siams.med.api.DrDzHD) | optional |  |
| morph_class | [RBiNK0366](#com.siams.med.api.RBiNK0366) | optional |  |
| tumor_main | [DrDzTM](#com.siams.med.api.DrDzTM) | optional |  |
| tumor_side | [DrDzTS](#com.siams.med.api.DrDzTS) | optional |  |
| plural | [DrDzPl](#com.siams.med.api.DrDzPl) | optional |  |






<a name="com.siams.med.api.TNM"/>

### TNM



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| t | [TnmT](#com.siams.med.api.TnmT) | optional |  |
| n | [TnmN](#com.siams.med.api.TnmN) | optional |  |
| m | [TnmM](#com.siams.med.api.TnmM) | optional |  |
| g | [TnmG](#com.siams.med.api.TnmG) | optional |  |





 

 

 

 



<a name="directories.proto"/>
<p align="right"><a href="#top">Top</a></p>

## directories.proto



<a name="com.siams.med.api.AddressType"/>

### AddressType
Запись справочника &#34;Тип адреса&#34;
* HP(&#34;Адрес регистрации&#34;),
* H(&#34;Адрес фактического проживания&#34;),
* NULL(&#34;Адрес места рождения&#34;),
* WP(&#34;Служебный адрес&#34;),
* DIR(&#34;Прямой почтовый или телекоммуникационный адрес рабочего места&#34;),
* PUB(&#34;Общий почтовый или телекоммуникационный адрес рабочего места&#34;),
* BAD(&#34;Неправильный адрес&#34;),
* TMP(&#34;Временный адрес&#34;),
* PST(&#34;Адрес для писем&#34;);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.BloodType"/>

### BloodType
Запись справочника &#34;Группа крови&#34;
* I_N(&#34;0(I)Rh-&#34;),
* I_P(&#34;0(I)Rh&#43;&#34;),
* II_N(&#34;A(II)Rh-&#34;),
* II_P(&#34;A(II)Rh&#43;&#34;),
* III_N(&#34;B(III)Rh-&#34;),
* III_P(&#34;B(III)Rh&#43;&#34;),
* IV_N(&#34;AB(IV)Rh-&#34;),
* IV_P(&#34;AB(IV)Rh&#43;&#34;);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.ChemKind"/>

### ChemKind

Запись справочника &#34;Вид химиотерапии&#34;
* NONE(&#34;неизвестно&#34;, null),
* SELF(&#34;самостоятельная&#34;, 1),
* ADJ(&#34;адъювантная&#34;, 2),
* NEO(&#34;неоадъювантная&#34;, 3);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.ClinicalGroupType"/>

### ClinicalGroupType
Запись справочника &#34;Клиническая группа&#34;
* NONE(&#34;&#34;, null),
* I(&#34;I&#34;, 1),
* I_a(&#34;Iа&#34;, 6),
* I_b(&#34;Iб&#34;, 7),
* II(&#34;II&#34;, 3),
* II_b(&#34;IIа&#34;, 2),
* III(&#34;III&#34;, 4),
* IV(&#34;IV&#34;, 5);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DiagnosticsType"/>

### DiagnosticsType
Запись справочника &#34;Тип диагностики&#34;
* OAM(&#34;ОАМ&#34;),
* OAK(&#34;ОАК&#34;),
* BAB(&#34;биохимия крови&#34;),
* X_RAY_CHEST(&#34;рентгенография грудной клетки&#34;),
* X_RAY_GORT(&#34;рентгенография гортани&#34;),
* FLS(&#34;ФЛС&#34;),
* FBS(&#34;ФБС&#34;),
* US_ABDOMINAL(&#34;УЗИ брюшной полости&#34;),
* US_PELVIC(&#34;УЗИ малого таза&#34;),
* MRT_PELVIC(&#34;МРТ малого таза&#34;),
* KT_CHEST(&#34;КТ грудной клетки&#34;),
* KT_ABDOMINAL(&#34;КТ брюшной полости&#34;),
* MRT_ABDOMINAL(&#34;МРТ брюшной полости&#34;),
* MRT_CNS(&#34;МРТ ЦНС&#34;),
* KT_H_N(&#34;КТ головы и шеи&#34;),
* US_MAM_GLAND(&#34;УЗИ молочных желез&#34;),
* MAMMO(&#34;маммография&#34;),
* FGDS(&#34;ФГДС&#34;),
* X_RAY_STOMACH(&#34;рентгенография желудка/пищевода&#34;),
* FKS(&#34;ФКС&#34;),
* IRRIGOSCOPY(&#34;ирригоскопия&#34;),
* GINEK_CITOLOG(&#34;гинекологический осмотр&#34;),
* HISTOLOGY(&#34;гистология&#34;),
* CYTOLOGY(&#34;цитология&#34;),
* PSA(&#34;ПСА&#34;),
* TRUZI(&#34;ТРУЗИ&#34;),
* CISTOSCOP(&#34;цистоскопия&#34;);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DoseUnit"/>

### DoseUnit

Запись справочника &#34;Единица измерения дозы&#34;
* NONE(&#34;&#34;, null),
* G(&#34;г&#34;, 1),
* MG(&#34;мг&#34;, 2),
* MKG(&#34;мкг&#34;, 3),
* ML(&#34;мл&#34;, 4),
* MG_DAY(&#34;мг/сут&#34;, 5),
* MKG_DAY(&#34;мкг/сут&#34;, 6),
* MLN_ED(&#34;млн ЕД&#34;, 7);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrAutopsy"/>

### DrAutopsy

Запись справочника &#34;Аутопсия&#34;
* id =  1 - не проводилась
* id =  2 - проводилась
* id =  3 - проводилась, результат неизвестен
* id =  0 - неизвестно, проводилась ли


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzHD"/>

### DrDzHD

Запись справочника &#34;Обстоятельства выявления&#34;
* id = 0 - неизвестно
* id = 1 - обратился сам
* id = 2 - активно при профосмотре
* id = 3 - активно в смотровом кабинете
* id = 4 - при других обстоятельствах
* id = 5 - посмертно при аутопсии
* id = 6 - посмертно без аутопсии


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzMthd"/>

### DrDzMthd

Запись справочника &#34;Метод подтверждения диагноза&#34;
* id = 0 - неизвестно
* id = 1 - морфологический
* id = 2 - цитологический
* id = 3 - эксплоративная операция
* id = 4 - лабораторно-инструментальный
* id = 5 - только клинический


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzPl"/>

### DrDzPl

Запись справочника &#34;Наличие первично-множественной опухоли&#34;
* id = 0 - неизвестно
* id = 1 - нет
* id = 2 - метахронная
* id = 3 - синхронная
* id = 4 - синхронно-метахронная


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzPr"/>

### DrDzPr

Запись справочника первичности установки диагноза
* id = -1 - не установлено
* id =  0 - неизвестно
* id =  1 - впервые
* id =  2 - повторно


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzRA"/>

### DrDzRA

Запись справочника &#34;Результат аутопсии&#34;
* id = 0 - неизвестно
* id = 1 - диагноз подтвержден
* id = 3 - диагноз изменен, другая локализация
* id = 4 - диагноз изменен, другой морфологический тип
* id = 5 - диагноз подтвержден &#43; другая локализация
* id = 6 - рак обнаружен при аутопсии
* id = 7 - диагноз не подтвержден


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzSt"/>

### DrDzSt

Запись справочника типа диагноза
* id = 1 - предварительный
* id = 9 - окончательный


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzTM"/>

### DrDzTM

Запись справочника &#34;Варианты значений основной опухоли диагноза&#34;
* id = -1 - неизвестно
* id =  0 - не основная
* id =  1 - основная


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzTS"/>

### DrDzTS

Запись справочника &#34;Варианты значений стороны опухоли диагноза&#34;
* id = 1 - слева
* id = 2 - справа
* id = 3 - двухсторонняя
* id = 4 - неприменимо


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrDzWO"/>

### DrDzWO

Запись справочника &#34;Причина поздней диагностики&#34;
* id = 0 - неизвестно
* id = 1 - скрытое течение болезни
* id = 2 - несвоевременное обращение
* id = 3 - отказ от обследования
* id = 4 - неполное обследование
* id = 5 - несовершенство диспансеризации
* id = 6 - ошибка клиническая
* id = 7 - ошибка рентгенологическая
* id = 8 - ошибка морфологическая
* id = 9 - ошибки других специалистов
* id = 10 - другие причины


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrNK0439"/>

### DrNK0439
Запись справочника &#34;Классификатор осложнений лечения злокачественного новообразования&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrNK0465"/>

### DrNK0465
справочник операций


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrPrsG"/>

### DrPrsG

Запись справочника вариантов значений пола человека
* id = 1 - М
* id = 2 - Ж
* id = 3 - не определено


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DrugType"/>

### DrugType

Запись справочника &#34;Тип препарата&#34;
* NONE(&#34;&#34;, null, &#34;&#34;),
* CTX(&#34;химиотерапия&#34;, 1, &#34;Э&#34;),
* HT(&#34;гормонотерапия&#34;, 2, &#34;Ю&#34;),
* ANY(&#34;лекарственная терапия&#34;, 3, &#34;Я&#34;);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.DzStage"/>

### DzStage

Запись справочника &#34;Стадия опухолевого процесса&#34;
* NONE(&#34;&#34;, null),
* I(&#34;I&#34;, 4),
* I_A(&#34;Ia&#34;, 1),
* I_B(&#34;Ib&#34;, 2),
* I_C(&#34;Ic&#34;, 3),
* II(&#34;II&#34;, 8),
* II_A(&#34;IIa&#34;, 5),
* II_B(&#34;IIb&#34;, 6),
* II_C(&#34;IIc&#34;, 7),
* III(&#34;III&#34;, 12),
* III_A(&#34;IIIa&#34;, 9),
* III_B(&#34;IIIb&#34;, 10),
* III_C(&#34;IIIc&#34;, 11),
* IV(&#34;IV&#34;, 16),
* IV_A(&#34;IVa&#34;, 13),
* IV_B(&#34;IVb&#34;, 14),
* IV_C(&#34;IVc&#34;, 15),
* IN_SITU(&#34;in situ&#34;, 17),
* NA(&#34;неприменимо&#34;, 18)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.LocMetType"/>

### LocMetType

Запись справочника &#34;Локализация отдаленных метастазов&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [LocMetType.Code](#com.siams.med.api.LocMetType.Code) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RBiFRV442"/>

### RBiFRV442

Запись справочника &#34;Классификатор социальных групп населения (для заполнения талона на оказание высокотехнологичной медицинской помощи)&#34; (1.2.643.5.1.13.2.1.1.439)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RBiMKB308"/>

### RBiMKB308

Запись справочника &#34;Международная классификация болезней и состояний,
связанных со здоровьем,  Десятого пересмотра. Версия 2&#34;
(1.2.643.5.1.13.2.1.1.641)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RBiNK0366"/>

### RBiNK0366

Запись справочника &#34;Морфологическая классификация новообразований&#34; (1.2.643.5.1.13.2.1.1.495)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RBiPRK438"/>

### RBiPRK438

Запись справочника &#34;Классификатор жителя города или села&#34; (1.2.643.5.1.13.2.1.1.573)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RBiPRP365"/>

### RBiPRP365

Запись справочника &#34;Классификатор профессий рабочих и должностей служащих&#34; (1.2.643.5.1.13.2.1.1.658)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RayKind"/>

### RayKind

Запись справочника &#34;Вид облучения&#34;
* NONE(&#34;Вид лучевой терапии неизвестен&#34;, null),
* PHOTON_RENT(&#34;Фотонная - рентгеновская близкофокусная&#34;, 1),
* PHOTON_RENT_DEEP(&#34;Фотонная - глубокая рентгенотерапия&#34;, 2),
* PHOTON_ENERGY_HIGH(&#34;Фотонная - тормозное излучение высоких энергий&#34;, 3),
* BETA(&#34;Бета - терапия&#34;, 4),
* GAMMA(&#34;Гамма - терапия&#34;, 5),
* CORP_ELECTRON(&#34;Корпускулярная - электронами&#34;, 6),
* CORP_HEAVY(&#34;Корпускулярная терапия тяжелыми заряженными частицами&#34;, 7),
* CORP_NEITRON(&#34;Корпускулярная - нейтронами&#34;, 8),
* PHOTON_ELECTRON(&#34;Сочетанная - фотонная и электронами&#34;, 9),
* PROTON_GAMMA(&#34;Сочетанная - протонами и гамма - терапия&#34;, 10),
* NEITRON_GAMMA(&#34;Сочетанная - нейтронами и гамма - терапия&#34;, 11),
* OTHER(&#34;Другие виды лучевой терапии&#34;, 12);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RayMethod"/>

### RayMethod

Запись справочника &#34;Метод облучения&#34;
* NONE(&#34;Метод лучевой терапии неизвестен&#34;, null),
* CONT_TISS(&#34;Непрерывная внутритканевая&#34;, 1),
* CONT_INCAV(&#34;Непрерывная внутриполостная&#34;, 2),
* CONT_I131(&#34;Непрерывная - I131&#34;, 3),
* CONT_AU198(&#34;Непрерывная - Au198&#34;, 4),
* FRA_2(&#34;Фракционирование традиционное (2 Гр)&#34;, 5),
* FRA_11(&#34;Фракционирование - дневное дробление (&gt;11 Гр 2 раза в день)&#34;, 6),
* FRA_3(&#34;Фракционирование - укрупненное (&gt; 3Гр)&#34;, 7),
* FRA_5(&#34;Фракционирование - укрупненное (&gt; 5Гр)&#34;, 8),
* FRA_DYN(&#34;Фракционирование - динамическое&#34;, 9),
* FRA_NOBREAK60(&#34;Фракционирование динамическое со сквозным курсом (без перерыва 60 Гр)&#34;, 10),
* FRA_BREAK30(&#34;Фракционирование динамическое с расщепленным курсом  (перерыв после 30 Гр)&#34;, 11),
* IRREG(&#34;С неравномерным облучением мишени (решетки и др.),&#34;, 12),
* TOTAL(&#34;Тотальная лучевая терапия&#34;, 13),
* SUBTOTAL(&#34;Субтотальная лучевая терапия&#34;, 14);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RayRadio"/>

### RayRadio

Запись справочника &#34;Радиомодификаторы&#34;
* NONE(&#34;неизвестно&#34;, null),
* GBO(&#34;ГБО&#34;, 1),
* CONT_INCAV(&#34;электронакцентные соединения&#34;, 2),
* HIPER_THERM(&#34;гипертермия&#34;, 3),
* HIPER_GLY(&#34;гипергликемия&#34;, 4),
* HYPO(&#34;гипоксия&#34;, 5),
* HIPOTHERM(&#34;гипотермия&#34;, 6),
* PREP(&#34;лекарственные препараты&#34;, 7),
* IMMUNO(&#34;иммуномодуляторы&#34;, 8),
* RADIO(&#34;радиофармпрепараты&#34;, 9),
* RADIO_SET(&#34;сочетание радиомодификаторов&#34;, 10),
* AOC(&#34;АОК - антиоксидантный комплекс&#34;, 11),
* WITHOUT(&#34;не использовались&#34;, 12);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RayWay"/>

### RayWay

Запись справочника &#34;Cпособ облучения&#34;
* NONE(&#34;неизвестно&#34;, null),
* EXT_DIST(&#34;внешнее дистанционное облучение&#34;, 1),
* EXT_APP(&#34;внешнее аппликационное облучение&#34;, 2),
* INCAV_CLO(&#34;внутриполостное облучение закрытыми источниками&#34;, 3),
* INCAV_OPN(&#34;внутриполостное облучение открытыми источниками&#34;, 4),
* TISS(&#34;внутритканевое облучение&#34;, 5),
* DIST_INCAV_CLO(&#34;дистанционное и внутриполостное облучение закрытыми источниками&#34;, 6),
* DIST_INCAV_OPN(&#34;дистанционное и внутриполостное облучение открытыми источниками&#34;, 7),
* DIST_TISS(&#34;дистанционное и внутритканевое облучение&#34;, 8),
* OTHER(&#34;другие способы облучения&#34;, 9);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RegInClause"/>

### RegInClause
Запись справочника &#34;Условия взятия на учет&#34;
* NONE(&#34;неизвестно&#34;, null),
* RI_A1(&#34;при жизни впервые&#34;, 1),
* RI_A2(&#34;при жизни повторно&#34;, 2),
* RI_M1(&#34;посмертно ранее нигде не стоял&#34;, 3),
* RI_M2(&#34;посмертно ранее состоял на учете&#34;, 4);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.RegOutReason"/>

### RegOutReason
Запись справочника &#34;Условия взятия на учет&#34;
* NONE(&#34;&#34;, null),
* RO_LEAVED(&#34;выехал&#34;, 1),
* RO_DS_REJECT(&#34;диагноз не подтвержден&#34;, 2),
* RO_BASAL(&#34;состоял по базалиоме&#34;, 3),
* RO_DIED_1(&#34;умер от причин связанных с основным заболеванием&#34;, 4),
* RO_DIED_2(&#34;умер от осложений лечения&#34;, 5),
* RO_DIED_3(&#34;умер от другого заболевания&#34;, 6);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.Srv59Chem"/>

### Srv59Chem

SPONKUSL	Справочник услуг при лечении онкологического заболевания
&lt;p&gt;
Утверждение структур электронных реестров персонифицированного учета медицинской помощи,
передаваемых при информационном взаимодействии между медицинскими организациями и
Территориальным фондом обязательного медицинского страхования Свердловской области в соответствии
с приказом ФФОМС от 30.03.2018 № 59
**Режим химиотерапии**
* SRV_2_2_1(&#34;Первая линия&#34;, 2, 2, 1),
* SRV_2_2_2(&#34;Вторая линия&#34;, 2, 2, 2),
* SRV_2_2_3(&#34;Третья линия&#34;, 2, 2, 3),
* SRV_2_2_4(&#34;Линия после третьей&#34;, 2, 2, 4),
* SRV_2_2_5(&#34;Адъювантная&#34;, 2, 2, 5),
* SRV_2_2_6(&#34;Неоадъювантная&#34;, 2, 2, 6),
* SRV_2_1_1(&#34;Первый цикл линии&#34;, 2, 1, 1),
* SRV_2_1_2(&#34;Последующие циклы линии (кроме последнего)&#34;, 2, 1, 2),
* SRV_2_1_3(&#34;Последний цикл линии (лечение прервано)&#34;, 2, 1, 3),
* SRV_2_1_4(&#34;Последний цикл линии (лечение завершено)&#34;, 2, 1, 4)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |
| group | [int32](#int32) | optional |  |
| index | [int32](#int32) | optional |  |






<a name="com.siams.med.api.Srv59Oper"/>

### Srv59Oper

SPONKUSL	Справочник услуг при лечении онкологического заболевания
&lt;p&gt;
Утверждение структур электронных реестров персонифицированного учета медицинской помощи,
передаваемых при информационном взаимодействии между медицинскими организациями и
Территориальным фондом обязательного медицинского страхования Свердловской области в соответствии
с приказом ФФОМС от 30.03.2018 № 59

* SRV_1_1_1(&#34;Первичной опухоли, в том числе с удалением регионарных лимфатических узлов&#34;, 1, 1, 1),
* SRV_1_1_2(&#34;Метастазов&#34;, 1, 1, 2),
* SRV_1_1_3(&#34;Симптоматическое&#34;, 1, 1, 3),
* SRV_1_1_4(&#34;Выполнено хирургическое стадирование&#34;, 1, 1, 4),
* SRV_1_1_5(&#34;Регионарных лимфатических узлов без первичной опухоли&#34;, 1, 1, 5),
* SRV_1_1_6(&#34;Циторедуктивное&#34;, 1, 1, 6),
* SRV_1_1_7(&#34;Паллиативное&#34;, 1, 1, 7),
* SRV_1_1_8(&#34;Операции с реконструктивно-пластическим компонентом, в т.ч. установка импланта&#34;, 1, 1, 8)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |
| group | [int32](#int32) | optional |  |
| index | [int32](#int32) | optional |  |






<a name="com.siams.med.api.Srv59Ray"/>

### Srv59Ray

SPONKUSL	Справочник услуг при лечении онкологического заболевания
&lt;p&gt;
Утверждение структур электронных реестров персонифицированного учета медицинской помощи,
передаваемых при информационном взаимодействии между медицинскими организациями и
Территориальным фондом обязательного медицинского страхования Свердловской области в соответствии
с приказом ФФОМС от 30.03.2018 № 59

* SRV_3_1_1(&#34;Первичной опухоли / ложа опухоли&#34;, 3, 1, 1),
* SRV_3_1_2(&#34;Лучевая терапия метастазов&#34;, 3, 1, 2),
* SRV_3_1_3(&#34;Симптоматическая лучевая терапия&#34;, 3, 1, 3)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |
| group | [int32](#int32) | optional |  |
| index | [int32](#int32) | optional |  |






<a name="com.siams.med.api.TherapyAim"/>

### TherapyAim

Запись справочника &#34;Применение терапии на этапах лечения&#34;
* NONE(&#34;неизвестно&#34;, null),
* PRIMARY(&#34;при лечении первичной опухоли&#34;, 1),
* RELAPSE(&#34;при лечении рецидива опухоли&#34;, 2),
* META(&#34;при лечении метастазов&#34;, 3),
* SYS(&#34;при лечении системных заболеваний&#34;, 4);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.TherapyCond"/>

### TherapyCond
Запись справочника &#34;Условия проведения лечения&#34;
* NONE(&#34;&#34;, null),
* AMB(&#34;амбулаторно&#34;, 1),
* HOSP(&#34;стационарно&#34;, 2);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.TnmG"/>

### TnmG

* NONE(&#34;&#34;),
* G_X(&#34;X&#34;),
* G_1(&#34;1&#34;),
* G_2(&#34;2&#34;),
* G_3(&#34;3&#34;),
* G_4(&#34;4&#34;);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.TnmM"/>

### TnmM

* NONE(&#34;&#34;, null),
* M_X(&#34;X&#34;, 1),
* M_0(&#34;0&#34;, 2),
* M_1(&#34;1&#34;, 3),
* M_1A(&#34;1a&#34;, 4),
* M_1B(&#34;1b&#34;, 5);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.TnmN"/>

### TnmN

* NONE(&#34;&#34;, null),
* N_X(&#34;X&#34;, 1),
* N_0(&#34;0&#34;, 2),
* N_1(&#34;1&#34;, 3),
* N_1A(&#34;1a&#34;, 4),
* N_1B(&#34;1b&#34;, 5),
* N_1C(&#34;1c&#34;, 6),
* N_2(&#34;2&#34;, 7),
* N_2A(&#34;2a&#34;, 8),
* N_2B(&#34;2b&#34;, 9),
* N_2C(&#34;2c&#34;, 10),
* N_3(&#34;3&#34;, 11),
* N_3A(&#34;3a&#34;, 12),
* N_3B(&#34;3b&#34;, 13),
* N_3C(&#34;3c&#34;, 14);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="com.siams.med.api.TnmT"/>

### TnmT

* NONE(&#34;&#34;, null),
* T_X(&#34;X&#34;, 1),
* T_0(&#34;0&#34;, 2),
* T_IS(&#34;is&#34;, 3),
* T_A(&#34;a&#34;, 4),
* T_1(&#34;1&#34;, 5),
* T_1A(&#34;1a&#34;, 6),
* T_1A1(&#34;1a1&#34;, 7),
* T_1A2(&#34;1a2&#34;, 8),
* T_1B(&#34;1b&#34;, 9),
* T_1C(&#34;1c&#34;, 10),
* T_2(&#34;2&#34;, 11),
* T_2A(&#34;2a&#34;, 12),
* T_2B(&#34;2b&#34;, 13),
* T_2C(&#34;2c&#34;, 14),
* T_3(&#34;3&#34;, 15),
* T_3A(&#34;3a&#34;, 16),
* T_3B(&#34;3b&#34;, 17),
* T_3C(&#34;3c&#34;, 18),
* T_4(&#34;4&#34;, 19),
* T_4A(&#34;4a&#34;, 20),
* T_4B(&#34;4b&#34;, 21),
* T_4C(&#34;4c&#34;, 22),
* T_4D(&#34;4d&#34;, 23);


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |





 


<a name="com.siams.med.api.LocMetType.Code"/>

### LocMetType.Code


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 1 | неизвестно |
| RLN | 2 | отдален. лимф. узлы |
| BONES | 4 | кости |
| LIVER | 8 | печень |
| LUNG | 16 | легкие и/или плевра |
| BRAIN | 32 | головной мозг |
| SKIN | 64 | кожа |
| KIDNEY | 128 | почки |
| OVARY | 256 | яичники |
| PERITONEUM | 512 | брюшина |
| BONE_MARROW | 1024 | костный мозг |
| OTHER_ORGANS | 2048 | другие органы |
| PLURAL | 4096 | множественные |


 

 

 



<a name="meta.proto"/>
<p align="right"><a href="#top">Top</a></p>

## meta.proto



<a name="com.siams.med.api.Object"/>

### Object



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| class_name | [string](#string) | required |  |
| meta | [Object.Entry](#com.siams.med.api.Object.Entry) | repeated |  |






<a name="com.siams.med.api.Object.Entry"/>

### Object.Entry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) | required |  |
| str | [string](#string) | optional |  |
| int32 | [int32](#int32) | optional |  |
| int64 | [int64](#int64) | optional |  |
| float | [float](#float) | optional |  |
| double | [double](#double) | optional |  |
| bool | [bool](#bool) | optional |  |
| date | [string](#string) | optional |  |






<a name="com.siams.med.api.Query"/>

### Query



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ids | [string](#string) | repeated |  |






<a name="com.siams.med.api.Update"/>

### Update



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| statement | [Update.Statment](#com.siams.med.api.Update.Statment) | repeated |  |






<a name="com.siams.med.api.Update.Statment"/>

### Update.Statment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| action | [Update.Action](#com.siams.med.api.Update.Action) | required |  |
| object_id | [string](#string) | required |  |
| meta | [Object.Entry](#com.siams.med.api.Object.Entry) | repeated |  |





 


<a name="com.siams.med.api.Update.Action"/>

### Update.Action


| Name | Number | Description |
| ---- | ------ | ----------- |
| SET | 1 |  |
| REMOVE | 2 |  |


 

 

 



<a name="oncor.proto"/>
<p align="right"><a href="#top">Top</a></p>

## oncor.proto



<a name="com.siams.med.api.Locality"/>

### Locality
Населенный Пункт


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional | Онкор id: #123:456 |
| name | [string](#string) | optional | Название населенного пункта: Екатерингбург, Владивосток,... |
| type | [string](#string) | optional | Тип населенного пункта: город, село, пгт,... |






<a name="com.siams.med.api.MedOrg"/>

### MedOrg



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| unq | [string](#string) | optional |  |
| name_full | [string](#string) | optional |  |
| name_short | [string](#string) | optional |  |
| kpp | [string](#string) | optional |  |
| ogrn | [string](#string) | optional |  |
| inn | [string](#string) | optional |  |
| okato | [string](#string) | optional |  |
| post_index | [string](#string) | optional |  |
| address | [string](#string) | optional |  |
| med_terr | [MedTerr](#com.siams.med.api.MedTerr) | optional |  |
| head_med_org_unq | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |






<a name="com.siams.med.api.MedTerr"/>

### MedTerr



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| unq | [string](#string) | optional |  |
| federal_code | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| name | [string](#string) | optional |  |
| okato | [string](#string) | optional |  |






<a name="com.siams.med.api.User"/>

### User



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| login | [string](#string) | optional |  |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| email | [string](#string) | optional |  |
| description | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| med_terr_id_set | [string](#string) | repeated |  |
| role_name_set | [string](#string) | repeated |  |





 

 

 

 



<a name="patients.proto"/>
<p align="right"><a href="#top">Top</a></p>

## patients.proto



<a name="com.siams.med.api.Address"/>

### Address



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| address | [string](#string) | optional |  |
| federal_code | [string](#string) | optional |  |
| region_code | [string](#string) | optional |  |
| town | [string](#string) | optional |  |
| street | [string](#string) | optional |  |
| house | [string](#string) | optional |  |
| flat | [string](#string) | optional |  |
| postal_code | [string](#string) | optional |  |
| fias | [string](#string) | optional |  |
| kladr | [string](#string) | optional |  |
| okato | [string](#string) | optional |  |
| med_terr | [MedTerr](#com.siams.med.api.MedTerr) | optional |  |
| locality | [Locality](#com.siams.med.api.Locality) | optional |  |
| type | [AddressType](#com.siams.med.api.AddressType) | optional |  |
| living_area_type | [RBiPRK438](#com.siams.med.api.RBiPRK438) | optional |  |






<a name="com.siams.med.api.EHR"/>

### EHR



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| patient_id | [string](#string) | optional |  |
| summary | [string](#string) | optional |  |
| dz | [ShortDz](#com.siams.med.api.ShortDz) | optional |  |






<a name="com.siams.med.api.Insurance"/>

### Insurance



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| insurance_number | [string](#string) | optional |  |






<a name="com.siams.med.api.Patient"/>

### Patient



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#com.siams.med.api.DrPrsG) | optional |  |
| code | [string](#string) | optional |  |
| ehr_count | [int32](#int32) | optional |  |
| blood_type | [BloodType](#com.siams.med.api.BloodType) | optional |  |
| social_status | [RBiFRV442](#com.siams.med.api.RBiFRV442) | optional |  |
| company_name | [string](#string) | optional |  |
| company_position | [RBiPRP365](#com.siams.med.api.RBiPRP365) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#com.siams.med.api.Insurance) | optional |  |
| phones | [string](#string) | optional |  |
| address | [Address](#com.siams.med.api.Address) | optional |  |






<a name="com.siams.med.api.PatientQuery"/>

### PatientQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#com.siams.med.api.DrPrsG) | optional |  |
| code | [string](#string) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#com.siams.med.api.Insurance) | optional |  |






<a name="com.siams.med.api.PatientSearchResult"/>

### PatientSearchResult
Результат, возвращаемый по запросу
```
GET /patient/search?name=Иванов%20Иван%20Иванович&amp;dob=311288&amp;gender=M&amp;limit=20
```


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| patients | [Patient](#com.siams.med.api.Patient) | repeated |  |
| warnings | [string](#string) | repeated |  |
| invalid_query_format | [bool](#bool) | optional |  |
| out_of_limit | [bool](#bool) | optional |  |






<a name="com.siams.med.api.PatientUpdate"/>

### PatientUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| entry | [PatientUpdate.Entry](#com.siams.med.api.PatientUpdate.Entry) | repeated |  |






<a name="com.siams.med.api.PatientUpdate.Entry"/>

### PatientUpdate.Entry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#com.siams.med.api.DrPrsG) | optional |  |
| blood_type | [BloodType](#com.siams.med.api.BloodType) | optional |  |
| social_status | [RBiFRV442](#com.siams.med.api.RBiFRV442) | optional |  |
| company_name | [string](#string) | optional |  |
| company_position | [RBiPRP365](#com.siams.med.api.RBiPRP365) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#com.siams.med.api.Insurance) | optional |  |
| phones | [string](#string) | optional |  |
| address | [Address](#com.siams.med.api.Address) | optional |  |





 

 

 

 



<a name="records.proto"/>
<p align="right"><a href="#top">Top</a></p>

## records.proto



<a name="com.siams.med.api.Drug"/>

### Drug

Запись справочника &#34;Препарат&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| name | [string](#string) | optional |  |
| type | [DrugType](#com.siams.med.api.DrugType) | optional |  |
| code | [string](#string) | optional |  |
| deleted | [bool](#bool) | optional |  |






<a name="com.siams.med.api.DrugRecord"/>

### DrugRecord



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| drug | [Drug](#com.siams.med.api.Drug) | optional |  |
| dose | [double](#double) | optional |  |
| unit | [DoseUnit](#com.siams.med.api.DoseUnit) | optional |  |






<a name="com.siams.med.api.Rc"/>

### Rc



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| class_name | [string](#string) | optional |  |
| patient_id | [string](#string) | optional |  |
| ehr_id | [string](#string) | optional |  |
| published | [Rc.Published](#com.siams.med.api.Rc.Published) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| summary | [string](#string) | optional |  |
| time_rc | [string](#string) | optional |  |
| attachment_id | [string](#string) | repeated |  |
| rc_doc | [Rc.RcDoc](#com.siams.med.api.Rc.RcDoc) | optional |  |
| rc_referral | [Rc.RcReferral](#com.siams.med.api.Rc.RcReferral) | optional |  |
| rc_appointment | [Rc.RcAppointment](#com.siams.med.api.Rc.RcAppointment) | optional |  |
| rc_dz | [Rc.RcDz](#com.siams.med.api.Rc.RcDz) | optional |  |
| rc_oper | [Rc.RcOper](#com.siams.med.api.Rc.RcOper) | optional |  |
| rc_ray | [Rc.RcRay](#com.siams.med.api.Rc.RcRay) | optional |  |
| rc_chem | [Rc.RcChem](#com.siams.med.api.Rc.RcChem) | optional |  |
| rc_horm | [Rc.RcHorm](#com.siams.med.api.Rc.RcHorm) | optional |  |
| rc_reg_in | [Rc.RcRegIn](#com.siams.med.api.Rc.RcRegIn) | optional |  |
| rc_reg_out | [Rc.RcRegOut](#com.siams.med.api.Rc.RcRegOut) | optional |  |
| rc_death | [Rc.RcDeath](#com.siams.med.api.Rc.RcDeath) | optional |  |
| rc_clinical_group | [Rc.RcClinicalGroup](#com.siams.med.api.Rc.RcClinicalGroup) | optional |  |






<a name="com.siams.med.api.Rc.Published"/>

### Rc.Published



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) | optional |  |
| time | [string](#string) | optional |  |






<a name="com.siams.med.api.Rc.RcAppointment"/>

### Rc.RcAppointment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| rc_referral_id | [string](#string) | optional |  |
| confirmed | [bool](#bool) | optional |  |
| department | [string](#string) | optional |  |
| doctor | [string](#string) | optional |  |
| consulting_room | [string](#string) | optional |  |
| consulting_date | [string](#string) | optional |  |
| note | [string](#string) | optional |  |






<a name="com.siams.med.api.Rc.RcChem"/>

### Rc.RcChem



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](date_time.md) окончания курса |
| org_unit_id | [string](#string) | optional | место проведения, [ссылка на справочник организаций](#com.siams.med.api.MedOrg) |
| aim | [TherapyAim](#com.siams.med.api.TherapyAim) | optional | применение на этапах лечения |
| kind | [ChemKind](#com.siams.med.api.ChemKind) | optional | вид |
| condition | [TherapyCond](#com.siams.med.api.TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#com.siams.med.api.DrNK0439) | optional | осложнение |
| drugs | [DrugRecord](#com.siams.med.api.DrugRecord) | repeated | препараты |
| srv | [Srv59Chem](#com.siams.med.api.Srv59Chem) | repeated | режим химиотерапии |






<a name="com.siams.med.api.Rc.RcClinicalGroup"/>

### Rc.RcClinicalGroup
запись &#34;Клиническая группа&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group_type | [ClinicalGroupType](#com.siams.med.api.ClinicalGroupType) | optional | Клиническая группа |






<a name="com.siams.med.api.Rc.RcDeath"/>

### Rc.RcDeath
запись &#34;Регистрация смерти&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| reason | [RBiMKB308](#com.siams.med.api.RBiMKB308) | optional | Причина смерти |
| autopsy | [DrAutopsy](#com.siams.med.api.DrAutopsy) | optional | Причина смерти |






<a name="com.siams.med.api.Rc.RcDoc"/>

### Rc.RcDoc



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| category | [string](#string) | optional |  |
| html | [string](#string) | optional |  |






<a name="com.siams.med.api.Rc.RcDz"/>

### Rc.RcDz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| diagnosis | [Dz](#com.siams.med.api.Dz) | optional |  |






<a name="com.siams.med.api.Rc.RcHorm"/>

### Rc.RcHorm



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](date_time.md) окончания курса |
| org_unit_id | [string](#string) | optional | место проведения, [ссылка на справочник организаций](#com.siams.med.api.MedOrg) |
| kind | [Rc.RcHorm.Kind](#com.siams.med.api.Rc.RcHorm.Kind) | optional | вид |
| aim | [TherapyAim](#com.siams.med.api.TherapyAim) | optional | применение на этапах лечения |
| condition | [TherapyCond](#com.siams.med.api.TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#com.siams.med.api.DrNK0439) | optional | осложнение |
| drugs | [DrugRecord](#com.siams.med.api.DrugRecord) | repeated | препараты |






<a name="com.siams.med.api.Rc.RcOper"/>

### Rc.RcOper



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| org_unit_id | [string](#string) | optional | место проведения, [ссылка на справочник организаций](../types/urg_unit_ref.md) |
| operation | [DrNK0465](#com.siams.med.api.DrNK0465) | optional | операция |
| condition | [TherapyCond](#com.siams.med.api.TherapyCond) | optional | условия проведения лечения |
| intra_compl | [DrNK0439](#com.siams.med.api.DrNK0439) | optional | интраоперационное осложнение |
| after_compl | [DrNK0439](#com.siams.med.api.DrNK0439) | optional | послеоперационное осложнение |
| srv | [Srv59Oper](#com.siams.med.api.Srv59Oper) | repeated | тип хирургического лечения |






<a name="com.siams.med.api.Rc.RcRay"/>

### Rc.RcRay



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](date_time.md) окончания курса |
| org_unit_id | [string](#string) | optional | место проведения, [ссылка на справочник организаций](#com.siams.med.api.MedOrg) |
| aim | [TherapyAim](#com.siams.med.api.TherapyAim) | optional | применение на этапах лечения |
| kind | [RayKind](#com.siams.med.api.RayKind) | optional | вид |
| method | [RayMethod](#com.siams.med.api.RayMethod) | optional | метод |
| way | [RayWay](#com.siams.med.api.RayWay) | optional | способ |
| radio | [RayRadio](#com.siams.med.api.RayRadio) | optional | радиомодификаторы |
| doze | [float](#float) | optional | суммарная доза на опухоль |
| doze_meta | [float](#float) | optional | суммарная доза на зоны регионарного метастазирования |
| condition | [TherapyCond](#com.siams.med.api.TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#com.siams.med.api.DrNK0439) | optional | осложнение |
| session_count | [int32](#int32) | optional | число сеансов |
| srv | [Srv59Ray](#com.siams.med.api.Srv59Ray) | repeated | тип лучевой терапии |






<a name="com.siams.med.api.Rc.RcReferral"/>

### Rc.RcReferral



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| rc_appointment_id | [string](#string) | optional |  |
| referral_org_unit_id | [string](#string) | optional |  |
| referral_type | [string](#string) | optional |  |
| purpose | [string](#string) | optional |  |
| routing_list | [RoutingList](#com.siams.med.api.RoutingList) | optional |  |






<a name="com.siams.med.api.Rc.RcRegIn"/>

### Rc.RcRegIn
запись постановки на учет


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| clause | [RegInClause](#com.siams.med.api.RegInClause) | optional | Условия взятия на учет |






<a name="com.siams.med.api.Rc.RcRegOut"/>

### Rc.RcRegOut
запись снятия с учета


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| reason | [RegOutReason](#com.siams.med.api.RegOutReason) | optional | Причина снятия с учета |





 

 

 

 



<a name="routing.proto"/>
<p align="right"><a href="#top">Top</a></p>

## routing.proto



<a name="com.siams.med.api.RoutingList"/>

### RoutingList



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| apply_last_on_any_other_disease_date | [string](#string) | optional | Date lastVisitOtherSickDate; Дата последнего обращения (госпитализации) по иному заболеванию |
| apply_last_date | [string](#string) | optional | Date lastVisitConsultantLPU; Дата последнего посещения профильной специальности |
| apply_first_date | [string](#string) | optional | Date firstComeLPUDate; Дата первого обращения в ЛПУ по месту жительства по поводу данного заболевания |
| request_date | [string](#string) | optional | Date oodConsultDatePlan; Дата формирования направления с места жительства в ОД // название лучше бы подошло refToODDate |
| admission_date | [string](#string) | optional | Date oodConsultDateFact; Дата фактического приема в ООД |
| examination_lsat_date | [string](#string) | optional | Date oodEndDiagDate; Дата окончания обследования в ОД |
| treatment_first_date | [string](#string) | optional | Date oodStartTherapyDate; дата начала лечения в ОД |
| health_record_code | [string](#string) | optional | String slNumber; номер больничного листа |
| expert_opinion | [string](#string) | optional | String expertConclusion; экспертное заключение |
| expert_opinion_date | [string](#string) | optional | Date expertConclusionDate; дата экспертного заключения |
| note | [string](#string) | optional | String comment; примечание |
| referral_code | [string](#string) | optional | String number; номер направления |
| diagnosis | [ShortDz](#com.siams.med.api.ShortDz) | optional |  |
| diagnostics | [RoutingList.Diagnostics](#com.siams.med.api.RoutingList.Diagnostics) | repeated |  |






<a name="com.siams.med.api.RoutingList.Diagnostics"/>

### RoutingList.Diagnostics



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [DiagnosticsType](#com.siams.med.api.DiagnosticsType) | optional |  |
| date | [string](#string) | optional |  |
| note | [string](#string) | optional |  |





 

 

 

 



<a name="search.proto"/>
<p align="right"><a href="#top">Top</a></p>

## search.proto



<a name="com.siams.med.api.Page"/>

### Page



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| job | [SearchJob](#com.siams.med.api.SearchJob) | required |  |
| offset | [int32](#int32) | optional |  |
| size | [int32](#int32) | optional |  |






<a name="com.siams.med.api.RcAppointmentQuery"/>

### RcAppointmentQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |






<a name="com.siams.med.api.RcDocQuery"/>

### RcDocQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| category | [string](#string) | optional |  |






<a name="com.siams.med.api.RcReferralQuery"/>

### RcReferralQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| has_appointment | [bool](#bool) | optional |  |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| from_org_unit_id | [string](#string) | optional |  |
| to_org_unit_id | [string](#string) | optional |  |






<a name="com.siams.med.api.RecordsPage"/>

### RecordsPage



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page | [Page](#com.siams.med.api.Page) | required |  |
| rc | [Rc](#com.siams.med.api.Rc) | repeated |  |
| size | [int32](#int32) | optional |  |






<a name="com.siams.med.api.SearchJob"/>

### SearchJob



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| ready | [bool](#bool) | optional |  |
| error | [ErrorResult](#com.siams.med.api.ErrorResult) | optional |  |





 

 

 

 



## Scalar Value Types

| .proto Type | Notes | C++ Type | Java Type | Python Type |
| ----------- | ----- | -------- | --------- | ----------- |
| <a name="double" /> double |  | double | double | float |
| <a name="float" /> float |  | float | float | float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long |
| <a name="bool" /> bool |  | bool | boolean | boolean |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str |

