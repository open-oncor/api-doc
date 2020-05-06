## Получение статуса медицинской записи

### ![GET](../../../img/get.png) /rc/getInstanceStatus`
* **URL parameter:** [id](../../../types/types.md#com.siams.med.api.Rc)
* **Response:** [[Rc](../../../types/types.md#com.siams.med.api.InstanceStatus)]

Возвращает объект типа [Rc](../../../types/types.md#com.siams.med.api.Rc) с идентификатором [id](../../../types/types.md#com.siams.med.api.Rc).

### Пример http

**Request**

GET `http://dev.onco-reg.ru/api/1.0/json/rc/getInstanceStatus HTTP/1.1`


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
        client.getInstanceStatus("1929:1");
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