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
          console.log('Connection failed. You can make something here');
      });

      ws.bind('TestChannel', {event_name: 'name'}, function(data) {
        console.log('Receiving data', data);
      });
    </script>
```
