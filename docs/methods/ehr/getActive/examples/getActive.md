[Работа с заболеваниями пациента](../../index.md)
==============================

### ![GET](../../../../img/get.png) [/ehr/getActive`?patient_id={patient_id}`](../index.md)

### Примеры

**Request:** GET `http://tempurl.com/ehr/getActive?patient_id=65:33650 HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "id":"#880:35540",
            "patient_id":"#65:33650",
            "summary":"",
            "dz":{
                "mkb_code":"C50.2",
                "mkb_name":"Верхневнутреннего квадранта молочной железы",
                "tnm":{
                    "t":{
                        "code":"NONE",
                        "caption":""
                    },
                    "n":{
                        "id":"2",
                        "code":"N_0",
                        "caption":"0"
                    },
                    "m":{
                        "code":"NONE",
                        "caption":""
                    },
                    "g":{
                        "code":"NONE",
                        "caption":""
                    }
                },
                "dz_stage":{
                    "code":"NONE",
                    "caption":""
                }
            }
        }
    ]
}
```