## Постраниченое получение найденных ранее в поисковом запросе записей


### ![POST](../../../../img/post.png) /search/get/RecordsPage
* **Request:** [Page](../../../../types/types.md#com.siams.med.api.Page) 
* **Response:** [RecordsPage](../../../../types/types.md#com.siams.med.api.RecordsPage)

Запрос выполняется после выполнения поискового запроса из группы `/search/start/*`.
Выполнение поискового запроса занимает время, которое зависит от величины выборки. 
Поэтому, при попытке получения записей нужно дождаться, чтобы поле `result.page.job.ready` установилось в `true`.
При этом поле `result.size` будет содержать общее количество записей, которые попали в поисковый запрос.
Для получения самих записей необходимо указать номер страницы (начиная с 0) в offset и
количество записей на странице в size.

### Структура сообщений ProtoBuffer

```proto

message Page {
    required SearchJob job = 1; //идентификатор SearchJob, полученный из запроса группы `/search/start/*`
    optional int32 offset = 2; //номер страницы, начиная с 0
    optional int32 size = 3; //количество записей на странице
}

message SearchJob {
    required string id = 1;
    oneof status {
        bool ready = 2; //признак готовности SearchJob. Если не true, то необходимо вновь повторить запрос 
        ErrorResult error = 3;
    }
}

message RecordsPage {
    required Page page = 1;
    repeated Rc rc = 2; //массив записей, полученных в ответе
    optional int32 size = 3; //общее количество записей, которые попали в поисковый запрос
}
 
 message RcTm66Order {
        optional Tm66OrderPurpose purpose = 1; // Цель дистанционного экспертного заключения
        optional Tm66DiagnosticsType diagnostics_type = 2; // Тип инструментальной диагностики
        optional string description = 3; // Краткое описание
        optional Tm66PrimaryDiagnosticsDoc primary_diagnostics_doc = 4; // Первичный протокол исследования
        repeated Tm66Doc docs = 5; // Медицинские документы
        optional MedResource client = 10; // Заказчик
        optional MO client_mo = 11; // МО заказчика
        optional MO expert_mo = 20; // МО исполнителя

        message Tm66PrimaryDiagnosticsDoc {
            optional Tm66DiagnosticsMethod method = 1; // Метод исследования
            optional string date_time = 2; // Дата и время проведения исследования
            optional string device = 3; // Аппарат, на котором проводилось исследование
            optional string text = 4; // Описание
            optional double dose_msv = 5; // Поглощенная доза (мЗв)
            repeated string attachment_id = 15; // Приложения
        }

        message Tm66Doc {
            optional string date_time = 2; // Дата и время проведения исследования
            optional string device = 3; // Аппарат, на котором проводилось исследование
            optional string text = 4; // Описание
            repeated string attachment_id = 15; // Приложения
        }
    }
```
### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/get/RecordsPage HTTP/1.1`
```json
{
    "page":{
        "job":{
            "id":"98a560e8-4c84-430e-8f7f-57c8c39d4c8e"
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
          "id": "98a560e8-4c84-430e-8f7f-57c8c39d4c8e",
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
          "id": "98a560e8-4c84-430e-8f7f-57c8c39d4c8e",
          "ready": true
        },
        "offset": 0,
        "size": 1
      },
      "rc": [
        {
          "id": "#1929:0",
          "class_name": "RcTm66Order",
          "patient_id": "#71:16260",
          "ehr_id": "#1055:16260",
          "published": {
            "user_id": "#961:0",
            "time": "2020-05-10 08:53:42"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-05-10 08:44:02",
          "rc_tm66_order": {
            "purpose": {
              "id": "5",
              "code": "ФОРМИРОВАНИЕ_ЭКСПЕРТНОГО_МНЕНИЯ",
              "caption": "Формирование экспертного мнения по результатам диагностических исследований (МСКТ, МРТ, ПЭТ-КТ и т.п.)"
            },
            "diagnostics_type": {
              "code": "РГ_ГРУДНОЙ_КЛЕТКИ",
              "caption": "Рентгенография органов грудной клетки"
            },
            "description": "",
            "primary_diagnostics_doc": {
              "method": {
                "code": "РГ",
                "caption": "Рентгенография"
              },
              "date_time": "2020-05-05 08:44:00",
              "device": "Philips CT",
              "text": "Текст заключения первичного исследования",
              "dose_msv": 15.0,
              "attachment_id": [
                "#1585:4532"
              ]
            },
            "docs": [
              {
                "date_time": "2020-05-12 08:45:00"
              }
            ]
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

