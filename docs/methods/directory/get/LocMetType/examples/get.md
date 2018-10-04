[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/LocMetType](../index.md)

### Примеры

**Request** \n GET `http://tempurl.com/directory/get/LocMetType HTTP/1.1`

**Response**
```json
{
    "result":[
        {
            "caption":"неизвестно",
            "code":"UNKNOWN"
        },
        {
            "caption":"отдален. лимф. узлы",
            "code":"RLN"
        },
        {
            "caption":"кости",
            "code":"BONES"
        },
        {
            "caption":"печень",
            "code":"LIVER"
        },
        {
            "caption":"легкие и/или плевра",
            "code":"LUNG"
        },
        {
            "caption":"головной мозг",
            "code":"BRAIN"
        },
        {
            "caption":"кожа",
            "code":"SKIN"
        },
        {
            "caption":"почки",
            "code":"KIDNEY"
        },
        {
            "caption":"яичники",
            "code":"OVARY"
        },
        {
            "caption":"брюшина",
            "code":"PERITONEUM"
        },
        {
            "caption":"костный мозг",
            "code":"BONE_MARROW"
        },
        {
            "caption":"другие органы",
            "code":"OTHER_ORGANS"
        },
        {
            "caption":"множественные",
            "code":"PLURAL"
        }
    ]
}
```