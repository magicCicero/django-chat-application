# docker-django-chat-room

## Execution

Navigate to this link [http://localhost:8000/chat/](http://localhost:8000/chat/)

If you want to chat you must register and login

Login in the login page

## How to execute

After verify you have installed docker, execute the following command

```cmd
docker-compose up
```

## Indications

I added a small JavaScript library that decorates the WebSocket API to provide a WebSocket connection that will automatically reconnect if the connection is dropped.
```javascript
...
$('#all_messages').scrollTop($('#all_messages')[0].scrollHeight);
var room_mame = '{{ room_name }}';
var ws_scheme = window.location.protocol == "https:" ? "wss" : "ws";
var websocket_str= ws_scheme+'://' + window.location.host + '/ws/chat/' + room_mame + '/';
var chatSocket = new ReconnectingWebSocket(websocket_str);
...
```

## Language used

* Python 3.8

## References and documentation

* [Django](https://www.djangoproject.com/)
* [Channels](https://github.com/django/channels)
* [reconnecting-websocket](https://github.com/joewalnes/reconnecting-websocket)
* [Design of the chat](https://bootsnipp.com/snippets/featured/chat-widget)

## License

MIT license
