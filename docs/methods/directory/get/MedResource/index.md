## Справочник врачей медицинских организаций

### ![GET](../../../../img/get.png) /directory/get/MedResource
* **Response: [[MedResource](../../../../types/types.md#com.siams.med.api.MedResource)]**

В ответе передаётся массив записей из справочника [MedResource](../../../../types/types.md#com.siams.med.api.MedResource).

Связанные справочники:
* [MedOrganization](../../../../methods/directory/get/MedOrganization/index.md) - `cправочник медицинских организаций `  
* [MedDepart](../../../../methods/directory/get/MedDepart/index.md) - `cправочник подразделений медицинских организаций ` 
### Пример http
**Request**  
GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/MedResource`

**Response**  
```json
{
  "result":[{"id":"140-660010-206(20170101)","code":"140-660010-206","date_range":["20170101","20181231"],"name":"ЗБИНСКАЯ Е И","doctor_code":"140","doctor_name":"ЗБИНСКАЯ Е И","med_org_code":"660010","med_spec_code":"206"},
            {"id":"140-660010-206(20190101)","code":"140-660010-206","date_range":["20190101","29991231"],"name":"ЗБИНСКАЯ Е И","doctor_code":"140","doctor_name":"ЗБИНСКАЯ Е И","med_org_code":"660010","med_spec_code":"206"},
            {"id":"220-660010-9(20170101)","code":"220-660010-9","date_range":["20170101","20170228"],"name":"КУЗНЕЦОВА Д С","doctor_code":"220","doctor_name":"КУЗНЕЦОВА Д С","med_org_code":"660010","med_spec_code":"9"},
            //...
            {"id":"220-660010-15(20170101)","code":"220-660010-15","date_range":["20170101","20181231"],"name":"КУЗНЕЦОВА Д С","doctor_code":"220","doctor_name":"КУЗНЕЦОВА Д С","med_org_code":"660010","med_spec_code":"15"}
          ]
} 
```