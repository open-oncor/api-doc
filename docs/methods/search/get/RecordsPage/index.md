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
 
message Rc {
    optional string id = 1;
    optional string class_name = 2;
    optional string patient_id = 3;
    optional string ehr_id = 4;
    optional Published published = 5;
    optional string org_unit_id = 6;

    optional string summary = 10;
    optional string time_rc = 11;

    repeated DeletedAt deleted_status = 14;
    repeated string attachment_id = 15;

    optional string instance_status = 16;

    message Published {
        optional string user_id = 1;
        optional string time = 2;
    }

    enum DeletedAt {
        RC = 1;
        EHR = 2;
        PTN = 3;
    }

    oneof rc {
        // ....
        RcTm66Order rc_tm66_order = 301;
        // ....
    }

    // ....

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
            optional string date_time = 2; // Дата и время документа
            optional string name = 3; // Наименование документа
            optional string description = 4; // Краткое описание
            repeated string attachment_id = 15; // Приложения
        }
    }

    // ....
}
```
### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/search/get/RecordsPage HTTP/1.1`
```json
{
    "page":{
        "job":{
            "id":"e3585aea-cf1c-4766-aa4b-afcf93c2d6d5"
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
          "id": "e3585aea-cf1c-4766-aa4b-afcf93c2d6d5",
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
          "id": "e3585aea-cf1c-4766-aa4b-afcf93c2d6d5",
          "ready": true
        },
        "offset": 0,
        "size": 1
      },
      "rc": [
        {
          "id": "#1929:2",
          "class_name": "RcTm66Order",
          "patient_id": "#71:16260",
          "ehr_id": "#1055:16260",
          "published": {
            "user_id": "#961:0",
            "time": "2020-05-11 09:47:42"
          },
          "org_unit_id": "#999:28",
          "time_rc": "2020-05-11 09:23:16",
          "rc_tm66_order": {
            "purpose": {
              "id": "5",
              "code": "ФОРМИРОВАНИЕ_ЭКСПЕРТНОГО_МНЕНИЯ",
              "caption": "Формирование экспертного мнения по результатам диагностических исследований (МСКТ, МРТ, ПЭТ-КТ и т.п.)"
            },
            "diagnostics_type": {
              "code": "КТ_ГРУДНОЙ_КЛЕТКИ",
              "caption": "Компьютерная томография грудной клетки"
            },
            "description": "Краткое описание заявки на ДЭЗО",
            "primary_diagnostics_doc": {
              "method": {
                "code": "КТ",
                "caption": "Компьютерная томография"
              },
              "date_time": "2020-05-01 09:24:00",
              "device": "Аппарат первичного исследования",
              "text": "Протокол первичного исследования (текст)",
              "dose_msv": 3.1,
              "attachment_id": [
                "#1585:4535"
              ]
            },
            "docs": [
              {
                "date_time": "2020-04-30 09:44:00",
                "name": "Прием онколого",
                "description": "Протокол приема онколога",
                "attachment_id": [
                  "#1586:4429"
                ]
              }
            ],
            "client": {
              "id": "4058-660893-206(20190617)",
              "code": "4058-660893-206",
              "dateRange": [
                "20190617",
                "29991231"
              ],
              "doctorCode": "4058",
              "doctorName": "ЛОБАРЕВ С В",
              "medOrgCode": "660893",
              "medSpecCode": "206"
            },
            "client_mo": {
              "id": "893(20190101)(20190101)",
              "code": "893(20190101)",
              "dateRange": [
                "20190101",
                "29991231"
              ],
              "name": "ГП 4 Н.Тагил",
              "longName": "Государственное бюджетное учреждение здравоохранения Свердловской области \"Городская поликлиника № 4 город Нижний Тагил\"",
              "medCode": "893",
              "terrCode": "1002",
              "address": "Свердловская обл., г. Нижний Тагил, ул. Новострой, д. 24",
              "phone": "8(3435)410412",
              "ogrn": "1026601382686",
              "chiefLastName": "Климова",
              "chiefFirstName": "Жанна",
              "chiefPatronymic": "Сергеевна"
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
              "terrCode": "1502",
              "address": "г. Екатеринбург, ул. Соболева, 29",
              "phone": "8(343)3561505",
              "ogrn": "1146658016614",
              "chiefLastName": "Елишев",
              "chiefFirstName": "Владимир",
              "chiefPatronymic": "Геннадьевич"
            }
          }
        }
      ],
      "size": 1
    }
  ]
}
```
