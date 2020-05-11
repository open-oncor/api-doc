## Справочник подразделений медицинских организаций

### ![GET](../../../../img/get.png) /directory/get/MedDepart
* **Response: [[MedDepart](../../../../types/types.md#com.siams.med.api.MedDepart)]**

В ответе передаётся массив записей из справочника [MedDepart](../../../../types/types.md#com.siams.med.api.MedDepart).

### Пример http

**Request**  
GET `http://{{ONCOR_API_HOST}}/api/1.0/json/directory/get/MedDepart`

**Response**
```json
{
  "result":[{"id":"90020000-660133(19930101)","code":"90020000-660133","dateRange":["19930101","20141231"],"departCode":"90020000","medOrgCode":"660133","nameFull":"Хирургическое отделение","nameShort":"Хирургическое","typeHelp":"3"},
    {"id":"90040000-660133(19930101)","code":"90040000-660133","dateRange":["19930101","20141231"],"departCode":"90040000","medOrgCode":"660133","nameFull":"Ортопедическое отделение","nameShort":"Ортопедическое","typeHelp":"3"},
    {"id":"20000-660113(19930101)","code":"20000-660113","dateRange":["19930101","20141231"],"departCode":"20000","medOrgCode":"660113","nameFull":"Пульмонологическое отделение","nameShort":"Пульмонологическое","typeHelp":"1"},
    {"id":"380000-661712(20080122)","code":"380000-661712","dateRange":["20080122","20121231"],"departCode":"380000","medOrgCode":"661712","nameFull":"Психиатрическое","nameShort":"Психиатрическое","typeHelp":"1"},
    {"id":"430000-661712(20080122)","code":"430000-661712","dateRange":["20080122","20121231"],"departCode":"430000","medOrgCode":"661712","nameFull":"Гнойной хирургии","nameShort":"Гнойной хирургии","typeHelp":"1"},
  
    {"id":"50000-660113(20180801)","code":"50000-660113","dateRange":["20180801","29991231"],"departCode":"50000","medOrgCode":"660113","nameFull":"Неврологическое отделение № 2","nameShort":"Неврологическое № 2","typeHelp":"1"}
  ]
}
```

