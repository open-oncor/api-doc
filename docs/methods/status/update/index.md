## Установка статуса медицинской записи

### ![POST](../../../img/post.png) /rc/updateInstanceStatus`
* **Request:** [InstanceStatus](../../../types/types.md#com.siams.med.api.InstanceStatus)
* **Response:** [InstanceStatus](../../../types/types.md#com.siams.med.api.InstanceStatus)

Возвращает объект типа [Rc](../../../types/types.md#com.siams.med.api.Rc) с идентификатором [id](../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/rc/updateInstanceStatus HTTP/1.1`
```json
{
   "updateInstanceStatus":{
       "json":"{status: \"Обработка началась\"}",
       "rc_id":"#1929:1"
   }
}

```

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

### Пример java

```java
public class RcStatusTest {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        Records.Rc rc = client.getRc("1929:1");
        String id = rc.getId();

        client.updateInstanceStatus(Records.InstanceStatus.newBuilder()
              .setRcId(rc.getId())
              .setJson("{status: \"Обработка началась\"}")
              .build());

    }
}
```

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