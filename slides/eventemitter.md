###  EventEmitter

Easy to use NodeJS module that provides:
```
class Group extends EventEmitter {
    ...
}

group.emit('newPeer', peer);
```


Somewhere else:
```
group.on('newPeer', (peer) => {
    
});
```