# Overview

- Javascript client to consumer websocket action cable for Rails
- This library isn't completed, but it is functional


## Example


```javascript

   <script src="websocket_actioncable_rails_client.js"></script>

   <script>
      var ws = new WebSocketActionCable('ws://localhost:28080/cable');

      ws.conexao(function(conexao) {
          if (conexao) {
              console.log('Connection ok');
              return;
          }
          console.log('Connection fails. Done anything here');
          return;
      });

      ws.bind('TestChannel', {evento: 1}, function(data) {
        console.log('Receiving data', data);
      });
    </script>
```
