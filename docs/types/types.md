# Protocol Documentation
<a name="top"/>

## Table of Contents

- [api.proto](#api.proto)
    - [ErrorResult](#ErrorResult)
    - [OnBehalf](#OnBehalf)
    - [Response](#Response)
    - [SuccessResult](#SuccessResult)
  
  
  
  

- [attachments.proto](#attachments.proto)
    - [Attachment](#Attachment)
    - [Attachment.Meta](#Attachment.Meta)
    - [Attachment.Query](#Attachment.Query)
  
  
  
  

- [diagnosis.proto](#diagnosis.proto)
    - [Dz](#Dz)
    - [ShortDz](#ShortDz)
    - [TNM](#TNM)
  
  
  
  

- [directories.proto](#directories.proto)
    - [AddressType](#AddressType)
    - [BloodType](#BloodType)
    - [ChemKind](#ChemKind)
    - [ClinicalGroupType](#ClinicalGroupType)
    - [DiagnosticsType](#DiagnosticsType)
    - [DoseUnit](#DoseUnit)
    - [DrAutopsy](#DrAutopsy)
    - [DrDzHD](#DrDzHD)
    - [DrDzMthd](#DrDzMthd)
    - [DrDzPl](#DrDzPl)
    - [DrDzPr](#DrDzPr)
    - [DrDzRA](#DrDzRA)
    - [DrDzSt](#DrDzSt)
    - [DrDzTM](#DrDzTM)
    - [DrDzTS](#DrDzTS)
    - [DrDzWO](#DrDzWO)
    - [DrNK0439](#DrNK0439)
    - [DrNK0465](#DrNK0465)
    - [DrPrsG](#DrPrsG)
    - [Drug](#Drug)
    - [DrugRecord](#DrugRecord)
    - [DrugType](#DrugType)
    - [DzStage](#DzStage)
    - [FRV442](#FRV442)
    - [KT0365](#KT0365)
    - [LocMet](#LocMet)
    - [LocMetType](#LocMetType)
    - [MedOrg](#MedOrg)
    - [MedOrgType](#MedOrgType)
    - [MedTerr](#MedTerr)
    - [PRK438](#PRK438)
    - [PRP365](#PRP365)
    - [RBiMKB308](#RBiMKB308)
    - [RBiNK0366](#RBiNK0366)
    - [RayKind](#RayKind)
    - [RayMethod](#RayMethod)
    - [RayRadio](#RayRadio)
    - [RayWay](#RayWay)
    - [RegInClause](#RegInClause)
    - [RegOutReason](#RegOutReason)
    - [Srv59Chem](#Srv59Chem)
    - [Srv59Oper](#Srv59Oper)
    - [Srv59Ray](#Srv59Ray)
    - [TherapyAim](#TherapyAim)
    - [TherapyCond](#TherapyCond)
    - [TnmG](#TnmG)
    - [TnmM](#TnmM)
    - [TnmN](#TnmN)
    - [TnmT](#TnmT)
    - [User](#User)
  
    - [LocMet.Code](#LocMet.Code)
  
  
  

- [meta.proto](#meta.proto)
    - [Object](#Object)
    - [Object.Entry](#Object.Entry)
    - [Query](#Query)
    - [Update](#Update)
    - [Update.Statment](#Update.Statment)
  
    - [Update.Action](#Update.Action)
  
  
  

- [patients.proto](#patients.proto)
    - [Address](#Address)
    - [EHR](#EHR)
    - [Insurance](#Insurance)
    - [Patient](#Patient)
    - [PatientQuery](#PatientQuery)
    - [PatientUpdate](#PatientUpdate)
    - [PatientUpdate.Entry](#PatientUpdate.Entry)
  
  
  
  

- [records.proto](#records.proto)
    - [Rc](#Rc)
    - [Rc.Published](#Rc.Published)
    - [Rc.RcAppointment](#Rc.RcAppointment)
    - [Rc.RcChem](#Rc.RcChem)
    - [Rc.RcClinicalGroup](#Rc.RcClinicalGroup)
    - [Rc.RcDeath](#Rc.RcDeath)
    - [Rc.RcDoc](#Rc.RcDoc)
    - [Rc.RcDz](#Rc.RcDz)
    - [Rc.RcHorm](#Rc.RcHorm)
    - [Rc.RcOper](#Rc.RcOper)
    - [Rc.RcRay](#Rc.RcRay)
    - [Rc.RcReferral](#Rc.RcReferral)
    - [Rc.RcRegIn](#Rc.RcRegIn)
    - [Rc.RcRegOut](#Rc.RcRegOut)
  
  
  
  

- [routing.proto](#routing.proto)
    - [RoutingList](#RoutingList)
    - [RoutingList.Diagnostics](#RoutingList.Diagnostics)
  
  
  
  

- [search.proto](#search.proto)
    - [Page](#Page)
    - [RcAppointmentQuery](#RcAppointmentQuery)
    - [RcDocQuery](#RcDocQuery)
    - [RcReferralQuery](#RcReferralQuery)
    - [RecordsPage](#RecordsPage)
    - [SearchJob](#SearchJob)
  
  
  
  

- [Scalar Value Types](#scalar-value-types)



<a name="api.proto"/>
<p align="right"><a href="#top">Top</a></p>

## api.proto



<a name="ErrorResult"/>

### ErrorResult



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) | required |  |
| message | [string](#string) | optional |  |
| uuid | [string](#string) | optional |  |






<a name="OnBehalf"/>

### OnBehalf



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| position | [string](#string) | optional |  |






<a name="Response"/>

### Response



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| success | [SuccessResult](#SuccessResult) | optional |  |
| error | [ErrorResult](#ErrorResult) | optional |  |






<a name="SuccessResult"/>

### SuccessResult






 

 

 

 



<a name="attachments.proto"/>
<p align="right"><a href="#top">Top</a></p>

## attachments.proto



<a name="Attachment"/>

### Attachment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| meta | [Attachment.Meta](#Attachment.Meta) | required |  |
| data | [bytes](#bytes) | required |  |






<a name="Attachment.Meta"/>

### Attachment.Meta



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| digest | [string](#string) | optional |  |
| name | [string](#string) | required |  |
| type | [string](#string) | required |  |
| size | [int64](#int64) | optional |  |
| created | [string](#string) | optional |  |






<a name="Attachment.Query"/>

### Attachment.Query



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ids | [string](#string) | repeated |  |





 

 

 

 



<a name="diagnosis.proto"/>
<p align="right"><a href="#top">Top</a></p>

## diagnosis.proto



<a name="Dz"/>

### Dz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| summary | [string](#string) | optional | Примечание |
| icd10 | [RBiMKB308](#RBiMKB308) | optional | МКБ10 |
| status | [DrDzSt](#DrDzSt) | optional | Тип диагноза |
| primacy | [DrDzPr](#DrDzPr) | optional | Первичность установки диагноза |
| morph_class | [RBiNK0366](#RBiNK0366) | optional | Морфологический тип |
| tumor_main | [DrDzTM](#DrDzTM) | optional | Признак основной опухоли |
| tumor_side | [DrDzTS](#DrDzTS) | optional | Сторона поражения |
| how_discover | [DrDzHD](#DrDzHD) | optional | Обстоятельства выявления |
| method | [DrDzMthd](#DrDzMthd) | optional | Метод подтверждения диагноза |
| plural | [DrDzPl](#DrDzPl) | optional | Наличие первично-множественной опухоли |
| res_autopsy | [DrDzRA](#DrDzRA) | optional | Результат аутопсии |
| why_old | [DrDzWO](#DrDzWO) | optional | Причина поздней диагностики |
| loc_met | [LocMet](#LocMet) | optional | Локализация отдаленных метастазов |
| tnm | [TNM](#TNM) | optional | TNM |
| stage | [DzStage](#DzStage) | optional | Стадия опухолевого процесса |






<a name="ShortDz"/>

### ShortDz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| summary | [string](#string) | optional |  |
| mkb_code | [string](#string) | optional |  |
| mkb_name | [string](#string) | optional |  |
| dz_date | [string](#string) | optional |  |
| tnm | [TNM](#TNM) | optional |  |
| dz_stage | [DzStage](#DzStage) | optional |  |
| how_discover | [DrDzHD](#DrDzHD) | optional |  |
| morph_class | [RBiNK0366](#RBiNK0366) | optional |  |
| tumor_main | [DrDzTM](#DrDzTM) | optional |  |
| tumor_side | [DrDzTS](#DrDzTS) | optional |  |
| plural | [DrDzPl](#DrDzPl) | optional |  |






<a name="TNM"/>

### TNM



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| t | [TnmT](#TnmT) | optional |  |
| n | [TnmN](#TnmN) | optional |  |
| m | [TnmM](#TnmM) | optional |  |
| g | [TnmG](#TnmG) | optional |  |





 

 

 

 



<a name="directories.proto"/>
<p align="right"><a href="#top">Top</a></p>

## directories.proto



<a name="AddressType"/>

### AddressType



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="BloodType"/>

### BloodType



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="ChemKind"/>

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






<a name="ClinicalGroupType"/>

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






<a name="DiagnosticsType"/>

### DiagnosticsType



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="DoseUnit"/>

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






<a name="DrAutopsy"/>

### DrAutopsy
Запись справочника &#34;Аутопсия&#34;
   id =  1 - не проводилась
   id =  2 - проводилась
   id =  3 - проводилась, результат неизвестен
   id =  0 - неизвестно, проводилась ли


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzHD"/>

### DrDzHD
Запись справочника &#34;Обстоятельства выявления&#34;
   id = 0 - неизвестно
   id = 1 - обратился сам
   id = 2 - активно при профосмотре
   id = 3 - активно в смотровом кабинете
   id = 4 - при других обстоятельствах
   id = 5 - посмертно при аутопсии
   id = 6 - посмертно без аутопсии


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzMthd"/>

### DrDzMthd
Запись справочника &#34;Метод подтверждения диагноза&#34;
   id = 0 - неизвестно
   id = 1 - морфологический
   id = 2 - цитологический
   id = 3 - эксплоративная операция
   id = 4 - лабораторно-инструментальный
   id = 5 - только клинический


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzPl"/>

### DrDzPl
Запись справочника &#34;Наличие первично-множественной опухоли&#34;
   id = 0 - неизвестно
   id = 1 - нет
   id = 2 - метахронная
   id = 3 - синхронная
   id = 4 - синхронно-метахронная


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzPr"/>

### DrDzPr
Запись справочника первичности установки диагноза
   id = -1 - не установлено
   id =  0 - неизвестно
   id =  1 - впервые
   id =  2 - повторно


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzRA"/>

### DrDzRA
Запись справочника &#34;Результат аутопсии&#34;
   id = 0 - неизвестно
   id = 1 - диагноз подтвержден
   id = 3 - диагноз изменен, другая локализация
   id = 4 - диагноз изменен, другой морфологический тип
   id = 5 - диагноз подтвержден &#43; другая локализация
   id = 6 - рак обнаружен при аутопсии
   id = 7 - диагноз не подтвержден


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzSt"/>

### DrDzSt
Запись справочника типа диагноза
   id = 1 - предварительный
   id = 9 - окончательный


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzTM"/>

### DrDzTM
Запись справочника &#34;Варианты значений основной опухоли диагноза&#34;
   id = -1 - неизвестно
   id =  0 - не основная
   id =  1 - основная


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzTS"/>

### DrDzTS
Запись справочника &#34;Варианты значений стороны опухоли диагноза&#34;
   id = 1 - слева
   id = 2 - справа
   id = 3 - двухсторонняя
   id = 4 - неприменимо


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrDzWO"/>

### DrDzWO
Запись справочника &#34;Причина поздней диагностики&#34;
   id = 0 - неизвестно
   id = 1 - скрытое течение болезни
   id = 2 - несвоевременное обращение
   id = 3 - отказ от обследования
   id = 4 - неполное обследование
   id = 5 - несовершенство диспансеризации
   id = 6 - ошибка клиническая
   id = 7 - ошибка ренгенологическая
   id = 8 - ошибка морфологическая
   id = 9 - ошибки других специалистов
   id = 10 - другие причины


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrNK0439"/>

### DrNK0439
Запись справочника &#34;Классификатор осложнений лечения злокачественного новообразования&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrNK0465"/>

### DrNK0465
справочник операций


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="DrPrsG"/>

### DrPrsG
Запись справочника вариантов значений пола человека
   id = 1 - М
   id = 2 - Ж
   id = 3 - не определено


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| id | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="Drug"/>

### Drug
Запись справочника &#34;Препарат&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) | optional |  |
| type | [DrugType](#DrugType) | optional |  |
| code | [string](#string) | optional |  |
| deleted | [bool](#bool) | optional |  |






<a name="DrugRecord"/>

### DrugRecord



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| drug | [Drug](#Drug) | required |  |
| dose | [double](#double) | optional |  |
| unit | [DoseUnit](#DoseUnit) | optional |  |






<a name="DrugType"/>

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






<a name="DzStage"/>

### DzStage
Запись справочника &#34;Стадия опухолевого процесса&#34;
 NONE(&#34;&#34;, null),
 I(&#34;I&#34;, 4),
 I_A(&#34;Ia&#34;, 1),
 I_B(&#34;Ib&#34;, 2),
 I_C(&#34;Ic&#34;, 3),
 II(&#34;II&#34;, 8),
 II_A(&#34;IIa&#34;, 5),
 II_B(&#34;IIb&#34;, 6),
 II_C(&#34;IIc&#34;, 7),
 III(&#34;III&#34;, 12),
 III_A(&#34;IIIa&#34;, 9),
 III_B(&#34;IIIb&#34;, 10),
 III_C(&#34;IIIc&#34;, 11),
 IV(&#34;IV&#34;, 16),
 IV_A(&#34;IVa&#34;, 13),
 IV_B(&#34;IVb&#34;, 14),
 IV_C(&#34;IVc&#34;, 15),
 IN_SITU(&#34;in situ&#34;, 17),
 NA(&#34;неприменимо&#34;, 18)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="FRV442"/>

### FRV442



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="KT0365"/>

### KT0365



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="LocMet"/>

### LocMet
Локализация отдаленных метастазов


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| codes | [LocMet.Code](#LocMet.Code) | repeated |  |






<a name="LocMetType"/>

### LocMetType
Запись справочника &#34;Локализация отдаленных метастазов&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [LocMet.Code](#LocMet.Code) | optional |  |
| caption | [string](#string) | optional |  |






<a name="MedOrg"/>

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
| med_terr | [MedTerr](#MedTerr) | optional |  |
| head_med_org_unq | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |






<a name="MedOrgType"/>

### MedOrgType



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="MedTerr"/>

### MedTerr



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| unq | [string](#string) | optional |  |
| federal_code | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| name | [string](#string) | optional |  |
| okato | [string](#string) | optional |  |






<a name="PRK438"/>

### PRK438



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="PRP365"/>

### PRP365



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| caption | [string](#string) | optional |  |






<a name="RBiMKB308"/>

### RBiMKB308
Запись справочника &#34;Международная классификация болезней и состояний,
связанных со здоровьем,  Десятого пересмотра. Версия 2&#34;
(1.2.643.5.1.13.2.1.1.641)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="RBiNK0366"/>

### RBiNK0366
Запись справочника &#34;Морфологическая классификация новообразований&#34; (1.2.643.5.1.13.2.1.1.495)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| orid | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="RayKind"/>

### RayKind
Запись справочника &#34;Вид облучения&#34;
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






<a name="RayMethod"/>

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






<a name="RayRadio"/>

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






<a name="RayWay"/>

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






<a name="RegInClause"/>

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






<a name="RegOutReason"/>

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






<a name="Srv59Chem"/>

### Srv59Chem
SPONKUSL	Справочник услуг при лечении онкологического заболевания
&lt;p&gt;
Утверждение структур электронных реестров персонифицированного учета медицинской помощи,
передаваемых при информационном взаимодействии между медицинскими организациями и
Территориальным фондом обязательного медицинского страхования Свердловской области в соответствии
с приказом ФФОМС от 30.03.2018 № 59

* SRV_4_1_1(&#34;Первичной опухоли / ложа опухоли&#34;, 4, 1, 1),
* SRV_4_1_2(&#34;Лучевая терапия метастазов&#34;, 4, 1, 2),
* SRV_4_1_3(&#34;Симптоматическая лучевая терапия&#34;, 4, 1, 3)


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |
| group | [int32](#int32) | optional |  |
| index | [int32](#int32) | optional |  |






<a name="Srv59Oper"/>

### Srv59Oper
SPONKUSL	Справочник услуг при лечении онкологического заболевания
&lt;p&gt;
Утверждение структур электронных реестров персонифицированного учета медицинской помощи,
передаваемых при информационном взаимодействии между медицинскими организациями и
Территориальным фондом обязательного медицинского страхования Свердловской области в соответствии
с приказом ФФОМС от 30.03.2018 № 59


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |
| group | [int32](#int32) | optional |  |
| index | [int32](#int32) | optional |  |






<a name="Srv59Ray"/>

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






<a name="TherapyAim"/>

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






<a name="TherapyCond"/>

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






<a name="TnmG"/>

### TnmG



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="TnmM"/>

### TnmM



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="TnmN"/>

### TnmN



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="TnmT"/>

### TnmT



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| code | [string](#string) | optional |  |
| caption | [string](#string) | optional |  |






<a name="User"/>

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





 


<a name="LocMet.Code"/>

### LocMet.Code


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



<a name="Object"/>

### Object



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| class_name | [string](#string) | required |  |
| meta | [Object.Entry](#Object.Entry) | repeated |  |






<a name="Object.Entry"/>

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






<a name="Query"/>

### Query



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ids | [string](#string) | repeated |  |






<a name="Update"/>

### Update



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| statement | [Update.Statment](#Update.Statment) | repeated |  |






<a name="Update.Statment"/>

### Update.Statment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| action | [Update.Action](#Update.Action) | required |  |
| object_id | [string](#string) | required |  |
| meta | [Object.Entry](#Object.Entry) | repeated |  |





 


<a name="Update.Action"/>

### Update.Action


| Name | Number | Description |
| ---- | ------ | ----------- |
| SET | 1 |  |
| REMOVE | 2 |  |


 

 

 



<a name="patients.proto"/>
<p align="right"><a href="#top">Top</a></p>

## patients.proto



<a name="Address"/>

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
| med_terr_unq | [string](#string) | optional |  |
| type | [AddressType](#AddressType) | optional |  |
| living_area_type | [PRK438](#PRK438) | optional |  |






<a name="EHR"/>

### EHR



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| patient_id | [string](#string) | optional |  |
| summary | [string](#string) | optional |  |
| dz | [ShortDz](#ShortDz) | optional |  |






<a name="Insurance"/>

### Insurance



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| insurance_number | [string](#string) | optional |  |






<a name="Patient"/>

### Patient



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#DrPrsG) | optional |  |
| code | [string](#string) | optional |  |
| ehr_count | [int32](#int32) | optional |  |
| blood_type | [BloodType](#BloodType) | optional |  |
| social_status | [FRV442](#FRV442) | optional |  |
| company_name | [string](#string) | optional |  |
| company_position | [PRP365](#PRP365) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#Insurance) | optional |  |
| phones | [string](#string) | optional |  |
| address | [Address](#Address) | optional |  |






<a name="PatientQuery"/>

### PatientQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#DrPrsG) | optional |  |
| code | [string](#string) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#Insurance) | optional |  |






<a name="PatientUpdate"/>

### PatientUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| code | [string](#string) | required |  |
| entry | [PatientUpdate.Entry](#PatientUpdate.Entry) | repeated |  |






<a name="PatientUpdate.Entry"/>

### PatientUpdate.Entry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| first_name | [string](#string) | optional |  |
| middle_name | [string](#string) | optional |  |
| last_name | [string](#string) | optional |  |
| birth_day | [string](#string) | optional |  |
| gender | [DrPrsG](#DrPrsG) | optional |  |
| blood_type | [BloodType](#BloodType) | optional |  |
| snils | [string](#string) | optional |  |
| insurance | [Insurance](#Insurance) | optional |  |
| phones | [string](#string) | optional |  |





 

 

 

 



<a name="records.proto"/>
<p align="right"><a href="#top">Top</a></p>

## records.proto



<a name="Rc"/>

### Rc



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | optional |  |
| class_name | [string](#string) | optional |  |
| patient_id | [string](#string) | optional |  |
| ehr_id | [string](#string) | optional |  |
| published | [Rc.Published](#Rc.Published) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| summary | [string](#string) | optional |  |
| time_rc | [string](#string) | optional |  |
| attachment_id | [string](#string) | repeated |  |
| rc_doc | [Rc.RcDoc](#Rc.RcDoc) | optional |  |
| rc_referral | [Rc.RcReferral](#Rc.RcReferral) | optional |  |
| rc_appointment | [Rc.RcAppointment](#Rc.RcAppointment) | optional |  |
| rc_dz | [Rc.RcDz](#Rc.RcDz) | optional |  |
| rc_oper | [Rc.RcOper](#Rc.RcOper) | optional |  |
| rc_ray | [Rc.RcRay](#Rc.RcRay) | optional |  |
| rc_chem | [Rc.RcChem](#Rc.RcChem) | optional |  |
| rc_horm | [Rc.RcHorm](#Rc.RcHorm) | optional |  |
| rc_reg_in | [Rc.RcRegIn](#Rc.RcRegIn) | optional |  |
| rc_reg_out | [Rc.RcRegOut](#Rc.RcRegOut) | optional |  |
| rc_death | [Rc.RcDeath](#Rc.RcDeath) | optional |  |
| rc_clinical_group | [Rc.RcClinicalGroup](#Rc.RcClinicalGroup) | optional |  |






<a name="Rc.Published"/>

### Rc.Published



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) | optional |  |
| time | [string](#string) | optional |  |






<a name="Rc.RcAppointment"/>

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






<a name="Rc.RcChem"/>

### Rc.RcChem



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](../types/date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](../types/date_time.md) окончания курса |
| aim | [TherapyAim](#TherapyAim) | optional | применение на этапах лечения |
| kind | [ChemKind](#ChemKind) | optional | вид |
| condition | [TherapyCond](#TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#DrNK0439) | optional | осложнение |
| org_id | [string](#string) | optional | место проведения |
| drugs | [DrugRecord](#DrugRecord) | repeated | препараты |
| srv | [Srv59Chem](#Srv59Chem) | repeated | тип |






<a name="Rc.RcClinicalGroup"/>

### Rc.RcClinicalGroup
запись &#34;Клиническая группа&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| group_type | [ClinicalGroupType](#ClinicalGroupType) | optional | Клиническая группа |






<a name="Rc.RcDeath"/>

### Rc.RcDeath
запись &#34;Регистрация смерти&#34;


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| reason | [RBiMKB308](#RBiMKB308) | optional | Причина смерти |
| autopsy | [DrAutopsy](#DrAutopsy) | optional | Причина смерти |






<a name="Rc.RcDoc"/>

### Rc.RcDoc



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| category | [string](#string) | optional |  |
| html | [string](#string) | optional |  |






<a name="Rc.RcDz"/>

### Rc.RcDz



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| diagnosis | [Dz](#Dz) | optional |  |






<a name="Rc.RcHorm"/>

### Rc.RcHorm



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](../types/date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](../types/date_time.md) окончания курса |
| kind | [Rc.RcHorm.Kind](#Rc.RcHorm.Kind) | optional | вид |
| aim | [TherapyAim](#TherapyAim) | optional | применение на этапах лечения |
| condition | [TherapyCond](#TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#DrNK0439) | optional | осложнение |
| org_id | [string](#string) | optional | место проведения |
| drugs | [DrugRecord](#DrugRecord) | repeated | препараты |






<a name="Rc.RcOper"/>

### Rc.RcOper



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| operation | [DrNK0465](#DrNK0465) | optional |  |
| condition | [TherapyCond](#TherapyCond) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| intra_compl | [DrNK0439](#DrNK0439) | optional |  |
| after_compl | [DrNK0439](#DrNK0439) | optional |  |
| srv | [Srv59Oper](#Srv59Oper) | repeated |  |






<a name="Rc.RcRay"/>

### Rc.RcRay



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| time_rc_in | [string](#string) | optional | [дата](../types/date_time.md) начала курса |
| time_rc_out | [string](#string) | optional | [дата](../types/date_time.md) окончания курса |
| aim | [TherapyAim](#TherapyAim) | optional | применение на этапах лечения |
| kind | [RayKind](#RayKind) | optional | вид |
| method | [RayMethod](#RayMethod) | optional | метод |
| way | [RayWay](#RayWay) | optional | способ |
| radio | [RayRadio](#RayRadio) | optional | радиомодификаторы |
| doze | [float](#float) | optional | суммарная доза на опухоль |
| doze_meta | [float](#float) | optional | суммарная доза на зоны регионарного метастазирования |
| condition | [TherapyCond](#TherapyCond) | optional | условия проведения |
| compl | [DrNK0439](#DrNK0439) | optional | осложнение |
| session_count | [int32](#int32) | optional | число сеансов |
| srv | [Srv59Ray](#Srv59Ray) | repeated | тип лучевой терапии |






<a name="Rc.RcReferral"/>

### Rc.RcReferral



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| rc_appointment_id | [string](#string) | optional |  |
| referral_org_unit_id | [string](#string) | optional |  |
| referral_type | [string](#string) | optional |  |
| purpose | [string](#string) | optional |  |
| routing_list | [RoutingList](#RoutingList) | optional |  |






<a name="Rc.RcRegIn"/>

### Rc.RcRegIn
запись постановки на учет


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| clause | [RegInClause](#RegInClause) | optional | Условия взятия на учет |






<a name="Rc.RcRegOut"/>

### Rc.RcRegOut
запись снятия с учета


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| reason | [RegOutReason](#RegOutReason) | optional | Причина снятия с учета |





 

 

 

 



<a name="routing.proto"/>
<p align="right"><a href="#top">Top</a></p>

## routing.proto



<a name="RoutingList"/>

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
| diagnosis | [ShortDz](#ShortDz) | optional |  |
| diagnostics | [RoutingList.Diagnostics](#RoutingList.Diagnostics) | repeated |  |






<a name="RoutingList.Diagnostics"/>

### RoutingList.Diagnostics



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [DiagnosticsType](#DiagnosticsType) | optional |  |
| date | [string](#string) | optional |  |
| note | [string](#string) | optional |  |





 

 

 

 



<a name="search.proto"/>
<p align="right"><a href="#top">Top</a></p>

## search.proto



<a name="Page"/>

### Page



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| job | [SearchJob](#SearchJob) | required |  |
| offset | [int32](#int32) | optional |  |
| size | [int32](#int32) | optional |  |






<a name="RcAppointmentQuery"/>

### RcAppointmentQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |






<a name="RcDocQuery"/>

### RcDocQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| org_unit_id | [string](#string) | optional |  |
| category | [string](#string) | optional |  |






<a name="RcReferralQuery"/>

### RcReferralQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| has_appointment | [bool](#bool) | optional |  |
| from_date | [string](#string) | optional |  |
| to_date | [string](#string) | optional |  |
| from_org_unit_id | [string](#string) | optional |  |
| to_org_unit_id | [string](#string) | optional |  |






<a name="RecordsPage"/>

### RecordsPage



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| page | [Page](#Page) | required |  |
| rc | [Rc](#Rc) | repeated |  |
| size | [int32](#int32) | optional |  |






<a name="SearchJob"/>

### SearchJob



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| id | [string](#string) | required |  |
| ready | [bool](#bool) | optional |  |
| error | [ErrorResult](#ErrorResult) | optional |  |





 

 

 

 



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
