## Получение списка заболеваний пациента

### ![GET](../../../img/get.png) /ehr/getList`?patient_id={patient_id}`
* **URL parameter:** [patient_id](../../../types/types.md#com.siams.med.api.EHR)
* **Response:** [[EHR](../../../types/types.md#com.siams.med.api.EHR)]

Возвращает список заболеваний пациента по ключу пациента.


### Пример http

**Request:** 

GET `http://dev.onco-reg.ru/api/1.0/json/ehr/getList?patient_id=65:33650 HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"#879:35649",
            "patient_id":"#65:33650",
            "summary":"",
            "dz":{
                "mkb_code":"C40.1",
                "mkb_name":"Коротких костей верхней конечности",
                "tnm":{
                    "t":{
                        "code":"NONE",
                        "caption":""
                    },
                    "n":{
                        "code":"NONE",
                        "caption":""
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
        },
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


### Пример java

```java
public class GetEhrList {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient;

        List<Patients.EHR> ehrList = client.getEHRList(patient.getId());
        Patients.EHR ehr = ehrList.get(0);

        String id = ehr.getId();
        Diagnosis.ShortDz dz = ehr.getDz();
    }
}
```

