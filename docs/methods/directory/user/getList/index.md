## Список пользователей

### ![GET](../../../../img/get.png) /user/getList
* **Response:** [[User](../../../../types/types.md#com.siams.med.api.User)]

Возвращает список пользователей [User](../../../../types/types.md#com.siams.med.api.User).



### Пример http
**Request** 
 
GET `https://demo.onco-reg.ru/api/1.0/json/user/getList HTTP/1.1
X-Oncor-API-Token: {{ONCOR_API_TOKEN}}
Content-Type: application/json`

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