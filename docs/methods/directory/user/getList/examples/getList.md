[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/user/getList](../index.md)

### Примеры

**Request** \n GET `http://tempurl.com/user/getList HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "id":"#961:0",
            "login":"admin",
            "first_name":"",
            "middle_name":"",
            "last_name":"",
            "org_unit_id":"#996:38",
            "role_name_set":[
                "Администратор"
            ]
        },
        {
            "id":"#961:1",
            "login":"SYSDBA@CR",
            "first_name":"Шабунина Любовь Анатольевна",
            "middle_name":"",
            "last_name":"CR",
            "org_unit_id":"#993:41",
            "role_name_set":[
                "System"
            ]
        },
        {
            "id":"#961:2",
            "login":"KIBALA@CR",
            "first_name":"Кибала Вероника",
            "middle_name":"",
            "last_name":"CR",
            "org_unit_id":"#993:41",
            "role_name_set":[
                "System"
            ]
        },
        ...
    ]
}
```