## Установка статуса медицинской записи

### ![POST](../../../img/post.png) /rc/updateInstanceStatus
* **Request:** [InstanceStatus](../../../types/types.md#com.siams.med.api.InstanceStatus)
* **Response:** [InstanceStatus](../../../types/types.md#com.siams.med.api.InstanceStatus)

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
###### Установка статуса "Обработка началась"
POST `http://{{ONCOR_API_HOST}}/api/1.0/json/rc/updateInstanceStatus HTTP/1.1`
```json
{
   "updateInstanceStatus":{
       "json":"{status: \"Обработка началась\"}",
       "rc_id":"#1929:2"
   }
}
```

###### Установка статуса "Ассоциация DICOM" c передачей ссылки на DICOM 
POST `http://{{ONCOR_API_HOST}}/api/1.0/json/rc/updateInstanceStatus HTTP/1.1`
```json
{
    "updateInstanceStatus":{
        "json":"{status: \"Ассоциация DICOM\", ris_dicom:\"http://ris_link_dicom\"}",
        "rc_id":"{{rcId}}"
    }
}
```

**Response**

###### Установка статуса "Обработка началась"

```json
{
  "result": [
    {
      "json": "{status: \"Обработка началась\"}",
      "rc_id": "#1929:2",
      "user_id": "#961:97",
      "time": "2020-05-11 09:54:22"
    }
  ]
}
```
###### Установка статуса "Ассоциация DICOM" c передачей ссылки на DICOM 
```json
{
  "result": [
    {
      "json": "{status: \"Ассоциация DICOM\", ris_dicom:\"http://ris_link_dicom\"}",
      "rc_id": "#1929:2",
      "user_id": "#961:97",
      "time": "2020-05-11 10:03:16"
    }
  ]
}
```
