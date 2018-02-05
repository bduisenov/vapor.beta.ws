# vapor.beta.ws

build and run
```$ swift build && .build/debug/Run```


swift code to pay attention:
https://github.com/bduisenov/vapor.beta.ws/blob/master/Sources/App/routes.swift#L30


connect to ws from client side and create ws onmessage hook
```js
var exampleSocket = new WebSocket("ws://my_token@localhost:8080/ws");

exampleSocket.onopen = function (event) {
  exampleSocket.send("Here's some text that the server is urgently awaiting!");
  };

exampleSocket.onmessage = function (event) {
  console.log(event.data);
  }

```

send message to server
```js
exampleSocket.send("Here's some text that the server is urgently awaiting!");
```
