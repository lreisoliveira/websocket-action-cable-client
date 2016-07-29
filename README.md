# Overview

- Javascript client to consumer websocket action cable for Rails
- This library isn't completed, but it is functional
 

## Example


```javascript

   <script src="websocket_actioncable_rails_client.js"></script>
   
   <script>

        ws = new WebSocketActionCable('ws://localhost:28080/cable');
        
        ws.subscriptions('TestChannel', {event_id: 1});
        
        // implement this function in your logic to use the data received from websocket
        function dataWebSocket(data) {
            console.log('Receiving data', data);
        }
    
    </script>

```

