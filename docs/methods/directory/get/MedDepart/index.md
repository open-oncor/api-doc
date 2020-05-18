## Справочник подразделений медицинских организаций

### ![GET](../../../../img/get.png) /directory/get/MedDepart
* **Response: [[MedDepart](../../../../types/types.md#com.siams.med.api.MedDepart)]**

В ответе передаётся массив записей из справочника [MedDepart](../../../../types/types.md#com.siams.med.api.MedDepart).

Связанные справочники:
* [MedOrganization](methods/directory/get/MedOrganization/index.md) - `cправочник медицинских организаций ` 
### Пример http

**Request**  
GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/MedDepart`

**Response**
```json
{
  "result":[{"id":"90020000-660133(19930101)","code":"90020000-660133","date_range":["19930101","20141231"],"name":"Хирургическое","depart_code":"90020000","med_org_code":"660133","name_full":"Хирургическое отделение","name_short":"Хирургическое","type_help":"3"},
            {"id":"90040000-660133(19930101)","code":"90040000-660133","date_range":["19930101","20141231"],"name":"Ортопедическое","depart_code":"90040000","med_org_code":"660133","name_full":"Ортопедическое отделение","name_short":"Ортопедическое","type_help":"3"},
            //...
            {"id":"120000-660709(20180705)","code":"120000-660709","date_range":["20180705","29991231"],"name":"Детское фтизиатрическое отделение № 2","depart_code":"120000","med_org_code":"660709","name_full":"Детское фтизиатрическое отделение № 2 , г. Екатеринбург, Сибирский тракт, д. 8, литер 21","name_short":"Детское фтизиатрическое отделение № 2","type_help":"1"},
            {"id":"50000-660113(20180801)","code":"50000-660113","date_range":["20180801","29991231"],"name":"Неврологическое № 2","depart_code":"50000","med_org_code":"660113","name_full":"Неврологическое отделение № 2","name_short":"Неврологическое № 2","type_help":"1"}
  ]
}
```

