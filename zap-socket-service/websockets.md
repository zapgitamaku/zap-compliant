# WebSockets

## WebSocket Client Implementation Documentation

This document provides a guide on how to implement the WebSocket client-side for the given WebSocket server implementation using socket.io.





{% hint style="info" %}
Note: Conversation Room broadcasts can only be received if the user/guest has joined a conversation room, by emitting the "login/guestLogin" event
{% endhint %}

### Setup

1. Install socket.io-client package in your front-end project:

```bash
npm install socket.io-client
```

2. Import socket.io-client and create a connection to the server:

```javascript
import { io } from "socket.io-client";

const socket = io("wss://api.zap.africa/");
```

### Events

The following events are available for the client-side implementation.

#### connected

The server emits this event when the client has connected successfully.

```javascript
socket.on("connected", (message) => {
  console.log(message); // "Connected to the socket.io server"
});
```

When a guest is connected,

```
socket.on("connected", ({guestId, socketId, message}) => {
  console.log(message); // "Connected to the socket.io server"
});
```

#### disconnected

The server emits this event when the client has connected successfully.

```javascript
socket.on("disconnected", (message) => {
  console.log(message); // "Connected to the socket.io server"
});
```

#### login

This event is emitted by the client to authenticate the user and associate their socket connection with their user ID, also to join a conversation Room.

```javascript
socket.emit("login", { userId: <USER_ID>, token: <JWT_TOKEN> });
```

#### supportLogin

This event is emitted by the client to authenticate the support user and associate their socket connection with their support ID, also to join a conversation Room.

```javascript
socket.emit("supportLogin", { userId: <USER_ID>, token: <JWT_TOKEN> });
```

#### guestLogin

This event is emitted by the client to register the guest and associate their socket connection with their guest ID. The connected event emitted by a server after this, contains the guestId

```javascript
socket.emit("guestLogin", { ipAddress: <IP_ADDRESS>});
```

#### supportMessage

This event is emitted by the client when a user sends a new support message. The server will then store the message and broadcast it to the conversation room.

```javascript
socket.emit("supportMessage", {
  userId: <USER_ID>,
  conversationId: <CONVERSATION_ID>,
  message: <MESSAGE_TEXT>,
});
```

#### supportGuestMessage

This event is emitted by the client when a guest sends a new support message. The server will then store the message and broadcast it to the conversation room.

```
socket.emit("supportGuestMessage", {
  userId: <GUEST_ID>,
  conversationId: <CONVERSATION_ID>,
  message: <MESSAGE_TEXT>,
});
```

#### supportGuestMessageFile

This event is emitted by the client when a guest sends a new support message. The server will then store the message and broadcast it to the conversation room.

```
socket.emit("supportGuestMessageFile", {
  userId: <GUEST_ID>,
  conversationId: <CONVERSATION_ID>,
   fileUrl: <FILE_URL>,
  fileType: <FILE_TYPE>,
});
```

#### supportUserMessage

This event is emitted by the client when a support user sends a new support message. The server will then store the message and broadcast it to the conversation room.

```javascript
socket.emit("supportUserMessage", {
  userId: <USER_ID>,
  conversationId: <CONVERSATION_ID>,
  message: <MESSAGE_TEXT>,
});
```

#### supportMessageFile

This event is emitted by the client when a user sends a new support message with a file. The server will broadcast the file to the conversation room.

```javascript
socket.emit("supportMessageFile", {
  userId: <USER_ID>,
  conversationId: <CONVERSATION_ID>,
  fileUrl: <FILE_URL>,
  fileType: <FILE_TYPE>,
});
```

#### supportUserMessageFile

This event is emitted by the client when a support user sends a new support message with a file. The server will broadcast the file to the conversation room.

```javascript
socket.emit("supportUserMessageFile", {
  userId: <USER_ID>,
  conversationId: <CONVERSATION_ID>,
  fileUrl: <FILE_URL>,
  fileType: <FILE_TYPE>,
});
```

#### markMessageAsRead

This event is emitted by the client when a user/supportUser reads a message. The server will then update the message and broadcast it to the conversation room.

```javascript
socket.emit("markMessageAsRead", {
  userId: <USER_ID>,
  messageId: <MESSAGE_ID>,
  conversationId: <CONVERSATION_ID>,
});
```

#### disconnect

This event is emitted by the client when the user disconnects from the WebSocket server.

```javascript
socket.disconnect();
```

### Listening for Events

The following events can be listened to on the client side.

#### error

This event is emitted by the server when the user fails to authenticate.

```javascript
socket.on("error", (error) => {
  console.error(error); // "UNAUTHORIZED_USER"
});
```

#### supportMessage

This event is emitted by the server when a new support message is received. The client can listen to this event to display the message in the conversation.

```javascript
socket.on("supportMessage", (message) => {
  console.log(message);
  // Display the message in the conversation
});
```

#### supportUserMessage

This event is emitted by the server when a new support user message is received. The client can listen to this event to display the message in the conversation.

<pre class="language-javascript"><code class="lang-javascript">socket.on("supportUserMessage", (message) => {
<strong>  console.log(message);
</strong>  // Display the message in the conversation
});
</code></pre>

#### supportMessageFile

This event is emitted by the server when a new support message with a file is received. The client can listen to this event to display the file in the conversation.

```javascript
socket.on("supportMessageFile", (file) => {
  console.log(file);
  // Display the file in the conversation
});
```



#### supportUserMessageFile

This event is emitted by the server when a new support message with a file is received. The client can listen to this event to display the file in the conversation.

```javascript
socket.on("supportUserMessageFile", (file) => {
  console.log(file);
  // Display the file in the conversation
});
```

#### updateMessage

This event is emitted by the server when a message is marked as read. The client can listen to this event to update the message in the conversation.

```javascript
socket.on("updateMessage", (data) => {
  console.log(data);
  // Update the message in the conversation
});
```

#### orderNotification

This event is emitted by the server when there's an update on the user's order(server receives user's funds). The client can listen to this event to display the update.

```javascript
socket.on("orderNotification", ({ orderId, amountReceived, orderAmount, confirmed, hash }) => {
  console.log(orderId, amountReceived, orderAmount, confirmed);
  // Update the UI with the order information
});
```

#### orderStatus

This event is emitted by the server when there's an update on the user's order(order status changes to verified). The client can listen to this event to display the update.

```javascript
socket.on("orderStatus", ({ orderId, orderStatus}) => {
  console.log(orderId, orderStatus);
  // Update the UI with the order information
});
```

#### conversationChange

This event is emitted by the server when a user/supportUser creates a message. The server will then update the conversation and broadcast it to the conversation room.

```javascript
socket.on("conversationChange", {
  conversationId: <CONVERSATION_ID>,
  message: <createdMessageData>
});
```

#### conversation

This event is emitted by the server when a user is added to a conversation and a new message is created in the coinversation. The client can listen to this event to display the conversation details.

```javascript
socket.on("conversation", (conversation) => {
  console.log(conversation);
  // Display the conversation details
});
```

\
