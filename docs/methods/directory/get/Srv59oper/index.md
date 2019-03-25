## Справочник услуг при лечении онкологического заболевания (приказ ФФОМС от 30.03.2018 № 59)

### ![GET](../../../../img/get.png) /directory/get/Srv59oper
* **Response: [[MedOrgType](../../../../types/types.md#com.siams.med.api.Srv59Oper)]**

В ответе передаётся массив записей из справочника [MedOrgType](../../../../types/types.md#com.siams.med.api.Srv59Oper).



### Пример http

**Request**  

GET `http://dev.onco-reg.ru/api/1.0/json/directory/get/Srv59Oper HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "code":"SRV_1_1_1",
            "caption":"Первичной опухоли, в том числе с удалением регионарных лимфатических узлов",
            "group":1,
            "index":1
        },
        {
            "code":"SRV_1_1_2",
            "caption":"Метастазов",
            "group":1,
            "index":2
        },
        {
            "code":"SRV_1_1_3",
            "caption":"Симптоматическое",
            "group":1,
            "index":3
        },
        {
            "code":"SRV_1_1_4",
            "caption":"Выполнено хирургическое стадирование",
            "group":1,
            "index":4
        },
        {
            "code":"SRV_1_1_5",
            "caption":"Регионарных лимфатических узлов без первичной опухоли",
            "group":1,
            "index":5
        },
        {
            "code":"SRV_1_1_6",
            "caption":"Циторедуктивное",
            "group":1,
            "index":6
        },
        {
            "code":"SRV_1_1_7",
            "caption":"Паллиативное",
            "group":1,
            "index":7
        },
        {
            "code":"SRV_1_1_8",
            "caption":"Операции с реконструктивно-пластическим компонентом, в т.ч. установка импланта",
            "group":1,
            "index":8
        }
    ]
}
```

### Пример java

```java
public class GetSrv59OperDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.Srv59Oper> srv59OperDirectory = client.getSrv59OperDirectory();
        Directories.Srv59Oper srv59Oper = srv59OperDirectory.get(0);

        String caption = srv59Oper.getCaption();
        String code = srv59Oper.getCode();
    }
}
```