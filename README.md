# Webchat

A simple IRC-like web chat server & client, implemented with SockJS.  Server runs on Node.js.

This project was primarily created to familiarize myself with Node & websockets.

## Instructions

### Server

Always runs on port 8000.  To change, edit server.js.

    node server.js

### Client

Point your browser to http://_your server_:8000/

The first client to join the chat will become the chatroom Op.  If the Op leaves the chatroom, one of the remaining members is randomly promoted to Op.

#### Commands

* /whisper, /w _nickname_ _message_ - sends a private message (whisper) to member.
* /emote, /e _message_ - 'emotes' the message
* /kick, /k _nickname_ - removes target member from chatroom.  Requires Op status.
* /mute, /m _nickname_ - mutes target member, preventing them from chatting or whispering.  Requires Op status.  Run /mute again to unmute.
* /promote, /p _nickname_ - promotes target member to Op.  Requires Op status.

## Node Dependencies

* connect - for serving static resources
* sockjs - websockets implementation for client-server communication

## Other Notes

Twitter Bootstrap is used for CSS/layout.
