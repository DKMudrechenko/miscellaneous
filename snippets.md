### Android Template Code Snippets

* [Playlists](#playlists)
* [Communication](#communication)

### Playlists

###### Set source by name

```java
setSource(String name) {
    Iterator iter = MediaGallery.getPlaylist().getSources();
    while (iter.hasNext()) {
        Source s = iter.next();
        if (s.getName().contains(name)) {
            MediaGallery.setSource(s);
        }
    }
}
```

###### Set source by index

```java
setSource(int idx) {
    int i = 0;
    for (Iterator iter = MeidaGallery.getPlaylist().getSources(); iter.hasNext();) {
        Source s = (Source)iter.next();
        if (i++ == idx) {
            MeidaGallery.setSource(s);
        }
    }
}
```


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
###### Broadcast command from script

```java
broadcastCommand(String name, String value) {
     Controller.sendCommand(name, value);
}
```

###### Listen for callbacks from a gadget

```java
Gadget.addOnCallbackListener(new OnCallbackListener() {
    onCallback(String[] args) {
        // do something
    }
});

