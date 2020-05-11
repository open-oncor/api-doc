## Справочник врачей медицинских организаций

### ![GET](../../../../img/get.png) /directory/get/MedResource
* **Response: [[MedResource](../../../../types/types.md#com.siams.med.api.MedResource)]**

В ответе передаётся массив записей из справочника [MedResource](../../../../types/types.md#com.siams.med.api.MedResource).

### Пример http
**Request**  
GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/MedResource`

**Response**  
```json
{
  "result":[{"id":"140-660010-206(20170101)","code":"140-660010-206","dateRange":["20170101","20181231"],"doctorCode":"140","doctorName":"ЗБИНСКАЯ Е И","medOrgCode":"660010","medSpecCode":"206"},
      {"id":"140-660010-206(20190101)","code":"140-660010-206","dateRange":["20190101","29991231"],"doctorCode":"140","doctorName":"ЗБИНСКАЯ Е И","medOrgCode":"660010","medSpecCode":"206"},
      {"id":"220-660010-9(20170101)","code":"220-660010-9","dateRange":["20170101","20170228"],"doctorCode":"220","doctorName":"КУЗНЕЦОВА Д С","medOrgCode":"660010","medSpecCode":"9"},
      {"id":"220-660010-15(20170101)","code":"220-660010-15","dateRange":["20170101","20181231"],"doctorCode":"220","doctorName":"КУЗНЕЦОВА Д С","medOrgCode":"660010","medSpecCode":"15"},
      {"id":"220-660010-37(20190101)","code":"220-660010-37","dateRange":["20190101","20190401"],"doctorCode":"220","doctorName":"КУЗНЕЦОВА Д С","medOrgCode":"660010","medSpecCode":"37"},

      {"id":"39925-661820-32(20200101)","code":"39925-661820-32","dateRange":["20200101","29991231"],"doctorCode":"39925","doctorName":"РУБЦОВА О И","medOrgCode":"661820","medSpecCode":"32"}
  ]
} 
```