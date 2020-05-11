## Получение статуса медицинской записи

### ![GET](../../../img/get.png) /rc/getInstanceStatus
* **URL parameter:** [id](../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../types/types.md#com.siams.med.api.InstanceStatus)]

### Структура сообщения ProtoBuffer

```proto
message InstanceStatus {
    optional string json = 1;
    optional string rc_id = 2;
    optional string user_id = 3;
    optional string time = 4;
    repeated InstanceStatus history = 5;
}
```

### Пример http

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/rc/getInstanceStatus?id=1929:1 HTTP/1.1`


**Response**

```json
{
 "result": [
   {
     "json": "{status: \"Обработка началась\"}",
     "rc_id": "#1929:1",
     "user_id": "#961:97",
     "time": "2020-05-06 10:06:24"
   }
 ]
}
```
