[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/TherapyCond](../index.md)

### Examples

**URI** GET `http://tempurl.com/directory/get/TherapyCond HTTP/1.1`

**Response**

```json
{
    "result":[
        {
            "code":"NONE",
            "caption":""
        },
        {
            "id":"1",
            "code":"AMB",
            "caption":"амбулаторно"
        },
        {
            "id":"2",
            "code":"HOSP",
            "caption":"стационарно"
        }
    ]
}
```