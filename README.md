# E-Chat
## About
An end-to-end encrypted messaging solution with Lightweight Directory Access Protocol user authentication.

Tools used:
-   NestJS
-   VueJs
-   Apache Directory Studio
-   Node-forge (for generating X509 requests)
<p align="center">
  <img width="750" src="readme-assets/Chat.png"/>
</p>


## Use Cases
<p align="center">
  <img width="750" src="readme-assets/Use-Case.png"/>
</p>

## Architecture
<p align="center">
  <img width="750" src="readme-assets/Architecture.png"/>
</p>

## Register Scenario
<p align="center">
  <img width="750" src="readme-assets/Register.png"/>
</p>

## WebSocket Messages
1) User Logs in, a **JOIN_CHAT** message is sent to the Server.
2) The server sends a **CONNECTED_USERS** with all connected users to clients.
3) Upon room joining, the client sends a **JOIN_ROOM** to the server, each two users have a uniuqe room.
4) Exchanging messages between users happen through a **MESSAGE** event to the server, each message is encrypted with the recipient's public Key, and decrypted with the reciever's private key (stored in local storage).