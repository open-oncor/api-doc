[Работа с пациентами](../../index.md)
==================================

### ![GET](../../../../../img/get.png) [/patient/record/getList`?patient_id={patient_id}`](../index.md)

### Examples

**URI** GET `http://tempurl/patient/record/getList?patient_id=65:33650 HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"#1577:16819",
            "class_name":"RcDoc",
            "patient_id":"#65:33650",
            "ehr_id":"#1049:33650",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-02 18:53:06"
            },
            "org_unit_id":"#999:28",
            "summary":"Проверяем /patient/record/add",
            "time_rc":"2018-10-02 18:53:06",
            "attachment_id":[
                "#1585:421"
            ],
            "rc_doc":{
                "category":"TEST",
                "html":"<b>Проверка Tue Oct 02 18:53:06 YEKT 2018</b>"
            }
        },
        {
            "id":"#1578:16804",
            "class_name":"RcDoc",
            "patient_id":"#65:33650",
            "ehr_id":"#1049:33650",
            "published":{
                "user_id":"#961:160",
                "time":"2018-10-02 18:58:12"
            },
            "org_unit_id":"#999:28",
            "summary":"Проверяем /patient/record/add",
            "time_rc":"2018-10-02 18:58:12",
            "attachment_id":[
                "#1586:412"
            ],
            "rc_doc":{
                "category":"TEST",
                "html":"<b>Проверка Tue Oct 02 18:58:12 YEKT 2018</b>"
            }
        }
    ]
}
```