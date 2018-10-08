[Работа со справочниками](../../../index.md)
=========================================

### ![GET](../../../../../img/get.png) [/user/getList](../index.md)

### Java пример

```java
public class GetUsers {
    public static void main(String[] args) throws IOException {
        ProtoBuffClient client = newProtoBuffClient();

        List<Directories.User> users = client.getUsers();
        Directories.User user = users.get(0);

        String id = user.getId();
        String login = user.getLogin();
    }
}

```

**[HTTP примеры](getList.md)**