[Работа с медицинскими записями](../index.md)
===============================

### ![GET](../../../../img/get.png) [/rc/getList`?ehr_id={ehr_id}`](../index.md)

### Примеры

**Request:** GET `http://tempurl.com/rc/getList?ehr_id=873:36386 HTTP/1.1`

**Response**
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