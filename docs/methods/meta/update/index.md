##Изменение метаданных для медицинской записи

### ![POST](../../../img/post.png) /meta/update
* **Request:** [Update](../../../types/types.md#com.siams.med.api.Update) 
* **Response:** [[Meta.proto](../../../types/types.md#metaproto)]

Обновляет метаданные [Meta.proto](../../../types/types.md#metaproto)

**Пример http**

**Request**

POST `http://dev.onco-reg.ru/api/1.0/json/meta/update HTTP/1.1`
```json
{
    "update":{
        "statement":[
            {
                "action":"SET",
                "object_id":"#65:33650",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#69:17722",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#66:21901",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#69:21247",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            },
            {
                "action":"SET",
                "object_id":"#70:29967",
                "meta":[
                    {
                        "name":"U:oncorApiUser:test",
                        "int64":2
                    }
                ]
            }
        ]
    }
}
```

**Response**

```json
{
    "result":[
        {
            "id":"#65:33650",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#69:17722",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#66:21901",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#69:21247",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        },
        {
            "id":"#70:29967",
            "class_name":"Ptn",
            "meta":[
                {
                    "name":"U:oncorApiUser:test",
                    "int64":2
                }
            ]
        }
    ]
}
```

**Пример java**

```java
public class QueryUpdate {
    public static void main(String[] args) throws IOException {
        final ProtoBuffClient client = newProtoBuffClient();
        final Meta.Update.Builder updateBuilder = Meta.Update.newBuilder();

        final List<Meta.Object> objects = getObjects();

        objects.forEach(o -> {
            final Meta.Update.Statment.Builder statement = Meta.Update.Statment.newBuilder();
            statement.setObjectId(o.getId());
            final String entryNameTest = "U:" + apiUser + ":exp";
            final Meta.Object.Entry newEntry = o.getMetaList().stream()
                    .filter(entry -> Objects.equals(entryNameTest, entry.getName())).findFirst()
                    .orElseGet(() -> Meta.Object.Entry.newBuilder()
                            .setName(entryNameTest)
                            .setInt64(0)
                            .build());
            if (newEntry.getInt64() < 2) {
                statement.setAction(Meta.Update.Action.SET);
                statement.addMeta(newEntry.toBuilder().setInt64(newEntry.getInt64() + 1).build());
            } else {
                statement.setAction(Meta.Update.Action.REMOVE);
            }
            updateBuilder.addStatement(statement);
        });

        client.updateMeta(updateBuilder.build());
    }
}
```