# 401-Read_12

## Questions

### Web Sockets

1. What is a Web Socket?
A WebSocket is a communication protocol that allows for real-time, two-way communication between a client (like a web browser) and a server over a single, long-lived connection.

2. Describe the Web Socket request/response handshake and what happens once the connection is established.
The WebSocket handshake is a special HTTP-based process used to initiate a WebSocket connection between the client and server. It's like saying:
        “Hey server, I’d like to switch from HTTP to WebSocket. Is that okay?”

    If the server agrees, the protocol switches and stays open for real-time communication.


3. Web Sockets provide a standardized way for the server to send content to a client without first receiving a **request** from that client.

### Socket.io Tutorial

1. What does the event handler io.on() do?
The `io.on()` method is an event handler used in `Socket.IO`, a popular JavaScript library that simplifies working with WebSockets.

It listens for a specific event (like a new client connection) on the server-side Socket.IO instance and lets you define a callback function to handle that event.

2. Describe some possible proof of life or proof that the code works as expected.
To confirm that your *WebSocket* or *Socket.IO* code is working correctly (i.e., proof of life), you can use several strategies to verify that the connection and communication are functioning as expected.
- console.log (server-side)
- console.log (client-side)
- Emit a Test Event and Receive a Response
- Network Tab in Browser Dev Tools

3. What does socket.emit() do?
The socket.emit() method is used to send a custom event and data from one side of a WebSocket (or Socket.IO) connection to the other — either from the client to the server, or from the server to a specific client.

### Socket.io vs Web Sockets

1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).
**WebSocket** is the *protocol*.
**Socket.IO** is a *library* built on top of WebSocket (plus other technologies) to make real-time communication easier, more reliable, and more powerful.

2. When would you use Socket.IO?
You would use Socket.IO when you need real-time, bidirectional communication between a client (browser) and a server, and you want a solution that is:
 ✅ Easy to use
 ✅ Reliable across all browsers and networks
 ✅ Feature-rich (with extras like reconnection, rooms, and namespaces)

3. When would you use WebSockets?
You would use WebSockets when you need a lightweight, low-latency, real-time connection between a client and server — especially when you want full control over the communication protocol and don’t need the extra features that libraries like Socket.IO provide.

## Videos

### OSI Model Explained

1. What are a couple of key takeaways from this video?
✅ **Key Takeaways** – *OSI Model*
- The OSI Model is a 7-layer framework that explains how data travels across a network.
- Each layer has a specific role, from user interaction (Layer 7) down to physical signals (Layer 1).
- It's mostly a conceptual tool, used for troubleshooting, learning, and communication between tech teams.
- Helps break down complex networking into manageable, logical steps.
- Commonly used to understand or explain issues in internet connections, software, and communication between systems.

### TCP Handshakes Explained

1. Translate the gist of this video to a non-technical friend
The TCP handshake is like two people making sure they’re both ready before starting a   phone call — a quick back-and-forth check that ensures the connection is solid before they start talking.


