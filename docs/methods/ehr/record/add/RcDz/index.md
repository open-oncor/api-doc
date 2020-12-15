## Добавление диагноза в указанное заболевание (RcDz)

### ![POST](../../../../../img/post.png) /ehr/record/add
* **Request:** [RcDz](../../../../../types/types.md#com.siams.med.api.Dz) **record** <patient_id, ehr_id, RcDz>
* **Response:** [[RcDz](../../../../../types/types.md#com.siams.med.api.Dz)]
* **Response`422`:**

Диагноз добавляется как запись [Rc](../../../../../types/types.md#com.siams.med.api.Rc) в указанное заболевание. Есди такой диагноз уже зарегистрирован у пациента ранее, метод вернёт ошибку.

### Пример http

**Request**

POST `https://demo.onco-reg.ru/api/1.0/json/ehr/record/add HTTP/1.1`
```json
{
    "record":{
        "patient_id":"#66:33481",
        "ehr_id":"#873:36386",
        "rc_dz":{
            "diagnosis":{
                "icd10":{
                    "code":"C50"
                },
                "status":{
                    "id":"1"
                },
                "primacy":{
                    "id":"1"
                },
                "morph_class":{
                    "code":"8001/3"
                },
                "tumor_main":{
                    "id":"-1"
                },
                "tumor_side":{
                    "id":"4"
                },
                "how_discover":{
                    "id":"0"
                },
                "method":{
                    "id":"0"
                },
                "plural":{
                    "id":"0"
                },
                "res_autopsy":{
                    "id":"0"
                },
                "why_old":{
                    "id":"10"
                },
                "loc_met":{
                    "codes":[
                        "UNKNOWN",
                        "OTHER_ORGANS"
                    ]
                },
                "tnm":{
                    "t":{
                        "code":"T_X"
                    },
                    "n":{
                        "code":"N_X"
                    },
                    "m":{
                        "code":"M_X"
                    },
                    "g":{
                        "code":"G_X"
                    }
                },
                "stage":{
                    "code":"NA"
                }
            }
        }
    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#881:45178",
            "class_name":"RcDz",
            "patient_id":"#66:33481",
            "ehr_id":"#873:36386",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-02 18:32:06"
            },
            "org_unit_id":"#999:28",
            "time_rc":"2018-10-02 18:32:04",
            "rc_dz":{
                "diagnosis":{
                    "summary":"",
                    "icd10":{
                        "orid":"#846:150",
                        "code":"C50",
                        "caption":"Злокачественное новообразование молочной железы"
                    },
                    "status":{
                        "orid":"#329:0",
                        "id":"1",
                        "caption":"предварительный"
                    },
                    "primacy":{
                        "orid":"#315:0",
                        "id":"1",
                        "caption":"впервые"
                    },
                    "morph_class":{
                        "orid":"#849:1",
                        "code":"8001/3",
                        "caption":"8001/3. Опухолевые клетки, злокачественные"
                    },
                    "tumor_main":{
                        "orid":"#337:0",
                        "id":"-1",
                        "caption":"неизвестно"
                    },
                    "tumor_side":{
                        "orid":"#350:0",
                        "id":"4",
                        "caption":"неприменимо"
                    },
                    "how_discover":{
                        "orid":"#289:0",
                        "id":"0",
                        "caption":"неизвестно"
                    },
                    "method":{
                        "orid":"#297:0",
                        "id":"0",
                        "caption":"неизвестно"
                    },
                    "plural":{
                        "orid":"#305:0",
                        "id":"0",
                        "caption":"неизвестно"
                    },
                    "res_autopsy":{
                        "orid":"#321:0",
                        "id":"0",
                        "caption":"неизвестно"
                    },
                    "why_old":{
                        "orid":"#356:1",
                        "id":"10",
                        "caption":"другие причины"
                    },
                    "loc_met":{
                        "codes":[
                            "OTHER_ORGANS",
                            "UNKNOWN"
                        ]
                    },
                    "tnm":{
                        "t":{
                            "id":"1",
                            "code":"T_X",
                            "caption":"X"
                        },
                        "n":{
                            "id":"1",
                            "code":"N_X",
                            "caption":"X"
                        },
                        "m":{
                            "id":"1",
                            "code":"M_X",
                            "caption":"X"
                        },
                        "g":{
                            "code":"G_X",
                            "caption":"X"
                        }
                    },
                    "stage":{
                        "id":"18",
                        "code":"NA",
                        "caption":"неприменимо"
                    }
                }
            }
        }
    ]
}
```

**Response `422`**
```json
{
    "error":{
        "name":"InvalidArgumentsException",
        "message":"Rc.ehr_id required",
        "uuid":"5f2ee073-bb3c-467d-afc4-275c411b27ca"
    }
}
```
