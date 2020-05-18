## Значимые исправления API

###  2020-05-18

* Изменилось именование полей **lowerCamelCase -> snake_case** следующих структур:
   * [MedOrganization](../../types/types.md#com.siams.med.api.MedOrganization)
   * [MedDepart](../../types/types.md#com.siams.med.api.MedDepart)
   * [MedResource](../../types/types.md#com.siams.med.api.MedResource)
* Изменились **Response**, в части этих структур, следующих методов:
  * [/directory/get/MedOrganization](../../methods/directory/get/MedOrganization/index.md) - `cправочник медицинских организаций `  
  * [/directory/get/MedDepart](../../methods/directory/get/MedDepart/index.md) - `cправочник подразделений медицинских организаций `  
  * [/directory/get/MedResource](../../methods/directory/get/MedResource/index.md) - `cправочник врачей медицинских организаций `
  * [/tm66/order/addRcTm66OrderReject](../../methods/tm66/order/addRcTm66OrderReject/index.md) - `загрузка документа "Отказ в проведении ДЭЗО"` 
  * [/tm66/order/addRcTm66OrderConclusion](../../methods/tm66/order/addRcTm66OrderConclusion/index.md) - `загрузка документа "Заключение эксперта ДЭЗО"`
  * [/tm66/order/addRcTm66OrderExpertiseDicom](../../methods/tm66/order/addRcTm66OrderExpertiseDicom/index.md) - `загрузка документа "Экспертиза качества DICOM"`
  * [/tm66/order/addRcTm66OrderExpertiseProtocol](../../methods/tm66/order/addRcTm66OrderExpertiseProtocol/index.md) - `загрузка документа "Экспертиза качества первичного протокола исследования"`
  * [/search/get/RecordsPage](../../methods/search/get/RecordsPage/index.md)  - `постраничное получение найденных ранее в поисковом запросе записей`