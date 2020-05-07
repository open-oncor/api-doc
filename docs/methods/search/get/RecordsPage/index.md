## Постраниченое получение найденных ранее в поисковом запросе записей


### ![POST](../../../../img/post.png) /search/get/RecordsPage
* **Request:** [Page](../../../../types/types.md#com.siams.med.api.Page) 
* **Response:** [RecordsPage](../../../../types/types.md#com.siams.med.api.RecordsPage)

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/get/RecordsPage HTTP/1.1`
```json
{
    "page":{
        "job":{
            "id":"43153f0a-9865-4943-a856-c30449d4eb0e"
        },
        "offset":0,
        "size":5
    }
}

```

**Response**

###### Ответ - не нашли не одной записи
```json
{
  "result": [
    {
      "page": {
        "job": {
          "id": "43153f0a-9865-4943-a856-c30449d4eb0e",
          "ready": true
        },
        "offset": 0,
        "size": 1
      },
      "size": 0
    }
  ]
}
```

###### Ответ - записи найдены
```json
{
 "result": [
   {
     "page": {
       "job": {
         "id": "43153f0a-9865-4943-a856-c30449d4eb0e",
         "ready": true
       },
       "offset": 0,
       "size": 1
     },
     "rc": [
       {
         "id": "#1929:1",
         "class_name": "RcTm66Order",
         "patient_id": "#68:31473",
         "ehr_id": "#1052:31473",
         "published": {
           "user_id": "#961:0",
           "time": "2020-05-06 09:58:32"
         },
         "org_unit_id": "#999:28",
         "time_rc": "2020-05-06 09:56:43",
         "rc_tm66_order": {
           "purpose": {
             "id": "2",
             "code": "ПОДТВЕРЖДЕНИЕ_ТАКТИКИ",
             "caption": "Определение (подтверждение) тактики лечения"
           },
           "diagnostics_type": {
             "code": "РГ_ЖЕЛУДКА_ПИЩЕВОДА",
             "caption": "Рентгенография желудка/пищевода"
           },
           "client_mo": {
             "id": "40(19960101)(19960101)",
             "code": "40(19960101)",
             "dateRange": [
               "19960101",
               "29991231"
             ],
             "name": "ГУЗ СО ПТД №4",
             "longName": "Государственное учреждение здравоохранения Свердловской области \"Противотуберкулезный диспансер №4\"",
             "medCode": "40",
             "terrCode": "901",
             "address": "Свердловская обл., г.Первоуральск, ул.Гагарина, 46",
             "phone": "8(3439)662219",
             "ogrn": "1036601471708",
             "chiefLastName": "Нестеров",
             "chiefFirstName": "Владимир",
             "chiefPatronymic": "Петрович"
           },
           "expert_mo": {
             "id": "1768(20190823)(20190823)",
             "code": "1768(20190823)",
             "dateRange": [
               "20190823",
               "29991231"
             ],
             "name": "СООД Екатеринбург",
             "longName": "Государственное автономное учреждение здравоохранения Свердловской области \"Свердловский областной онкологический диспансер\"",
             "medCode": "1768",
             "terrCode": "1502"
           }
         }
       }
     ],
     "size": 1
   }
 ]
}
```

### Пример java

```java
public class GetRecordsPage {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        final Search.SearchJob job = client.startSearchRcReferral(Search.RcReferralQuery.newBuilder()
                .setFromDate("2016-10-01")
                .setToDate("2019-12-10")
                .setHasAppointment(false)
                .build());

        final Search.RecordsPage recordsPage = client.getSearchRecordsPage(Search.Page.newBuilder()
                .setJob(job)
                .setOffset(0)
                .setSize(5)
                .build());

        Search.Page page = recordsPage.getPage();
    }
}
```

### Структура сообщений ProtoBuffer

```proto

message Page {
    required SearchJob job = 1;
    optional int32 offset = 2;
    optional int32 size = 3;
}

message RecordsPage {
    required Page page = 1;
    repeated Rc rc = 2;
    optional int32 size = 3;
}

```