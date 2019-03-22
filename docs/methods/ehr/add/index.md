## Регистрация заболевания пациента

### ![POST](../../../img/post.png) /ehr/add
* **Request:** [EHR](../../../types/types.md#com.siams.med.api.EHR) **ehr** <patient_id>
* **Response:** [[EHR](../../../types/types.md#com.siams.med.api.EHR)]
* **Response ```422```:** [ErrorResult](../../../types/types.md#com.siams.med.api.ErrorResult)

Регистрирует новое заболевание для пациента.  

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/ehr/add HTTP/1.1`
```json
{
    "ehr":{
        "patient_id":"#66:33481"
    }
}
```

**Response `200`**

```json
{
    "result":[
        {
            "id":"#873:36386",
            "patient_id":"#66:33481",
            "summary":""
        }
    ]
}
```

**Response `422`**
```json
{
    "error":{
        "name":"PatientNotFoundException",
        "message":"Patient \"\" not found",
        "uuid":"9b2ef941-b81d-43e3-8e87-e8b0dad6e6e2"
    }
}
```



### Пример java 

```java
public class AddEhr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Patients.Patient patient = getPatient();

        Patients.EHR ehr = client.addEHR(Patients.EHR.newBuilder()
                .setPatientId(patient.getId())
                .build());
        
        String id = ehr.getId();
        Diagnosis.ShortDz dz = ehr.getDz();
    }
}
```
