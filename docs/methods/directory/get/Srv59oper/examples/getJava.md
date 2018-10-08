[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/directory/get/Srv59oper](../index.md)

### Java пример

```java
public class GetSrv59OperDr {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.Srv59Oper> srv59OperDirectory = client.getSrv59OperDirectory();
        Directories.Srv59Oper srv59Oper = srv59OperDirectory.get(0);

        String caption = srv59Oper.getCaption();
        String code = srv59Oper.getCode();
    }
}
```

**[HTTP примеры](get.md)**