## Прямая ссылка на просмотр медицинской записи

###  /rc/ui-orid/`{rc_id}`

rc_id = Rc.id.substring(1) - значение [Rc.id]((../../../types/types.md#com.siams.med.api.Rc))  без первого символа "#"

### Структура сообщений ProtoBuffer
```proto
    message Rc {
        optional string id = 1;
    
        // ....
    }
```

### Пример http

`https://dev.onco-reg.ru/ui-orid/1937:3`