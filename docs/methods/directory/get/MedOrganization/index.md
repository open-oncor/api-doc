## Справочник медицинских организаций

### ![GET](../../../../img/get.png) /directory/get/MO
* **Response: [[MedOrganization](../../../../types/types.md#com.siams.med.api.MedOrganization)]**

В ответе передаётся массив записей из справочника [MedOrganization](../../../../types/types.md#com.siams.med.api.MedOrganization).

### Пример http

**Request**  
GET `https://demo.onco-reg.ru/api/1.0/json/directory/get/MedOrganization`  
`X-Oncor-API-Token: {{ONCOR_API_TOKEN}}`  
`Content-Type: application/json`


**Response**  
```json
{
  "result":[{"id":"660640(19960101)","code":"660640","date_range":["19960101","20030827"],"name":"АЯТСКАЯ Сельская УБ","mo_code":"640","long_name":"АЯТСКАЯ Сельская участковая Больница","med_org_code":"660640","terr_code":"1201","address":"Невьянский р-н с.Аятское ул.Ворошилова,1","phone":"34165","ogrn":"0","chief_last_name":"Рыжова","chief_first_name":"Надежда","chief_patronymic":"Викторовна"},
            {"id":"660640(20030828)","code":"660640","date_range":["20030828","20041124"],"name":"Амбулат. с.Аятское","mo_code":"640","long_name":"Амбулатория с.Аятское","med_org_code":"660640","terr_code":"1201","address":"Невьянский р-н с.Аятское ул.Ворошилова,1","phone":"34165","ogrn":"0","chief_last_name":"Рыжова","chief_first_name":"Надежда","chief_patronymic":"Викторовна"},
            {"id":"660640(20041125)","code":"660640","date_range":["20041125","20090828"],"name":"ФАП с.Аятское","mo_code":"640","long_name":"ФАП с.Аятское","med_org_code":"660640","terr_code":"1201","address":"Невьянский р-н с.Аятское ул.Ворошилова,1","phone":"34165","ogrn":"0","chief_last_name":"Рыжова","chief_first_name":"Надежда","chief_patronymic":"Викторовна"},
    //...
            {"id":"661079(19970101)","code":"661079","date_range":["19970101","20111231"],"name":"ШИЛОВСКИЙ ФАП","mo_code":"1079","long_name":"ШИЛОВСКИЙ ФАП","med_org_code":"661079","terr_code":"1301","address":"д. Шиловка","phone":"3-27-52","ogrn":"0","chief_last_name":"Макарова","chief_first_name":"Лариса","chief_patronymic":"Михайловна"}
           ]
}
```