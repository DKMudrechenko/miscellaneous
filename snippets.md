### Android Template Code Snippets

* [Communication](#communication)


### Communication

###### Listen for a remote command fom the server

```java
Controller.addOnCommandListener(new OnCommandListener() {
    onCommand(String name, String value) {
        if (name.equals("synchronize")) {
            // do something
        }
    }
});
```
