<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h4>Java ChatBox</h4>
    <p>This code represents a simple chat server implementation using sockets in Java. The server class acts as the main server,which listens 
        for incoming client connections and creates a seperate thread(connectionhandler) to handle each client.</p>
    <p>The server implements the Runnable interface, so it can be executed in a separate thread. In the run() method, it sets up the server socket, accepts client connections, 
        creates a new ConnectionHandler for each client, adds it to the connections list, and executes it in the thread pool.</p>
    <p>The Client class implements the Runnable interface, allowing it to be executed in a separate thread. In the run() method, it establishes a connection with the server by creating a socket and initializing the input and output streams. 
        It also creates an InputHandler object, which is responsible for reading user input from the console and sending it to the server. The InputHandler is executed in a separate thread.</p>
        <ul>
            <li>The broadcast() method sends a message to all connected clients by calling the sendMessage() method on each ConnectionHandler instance.</li>
        </ul>
        <ul>
            <li>The sendMessage() method sends a message to the client by writing it to the output stream.</li>
        </ul>
        <ul>
            <li>The shutdown() method is responsible for closing the input and output streams and the client socket.</li>
        </ul>
        <ul>
            <li>Finally, in the main() method, an instance of the server class is created, and the run() method is called to start the server in a separate thread.
                Similarly, main() method is created for the Client.
            </li>
        </ul>
        <ul>
            <li>This code represents a basic chat client that connects to a server and allows the user to send messages to the server and receive messages from other connected clients.
                 The user input is read from the console, and messages are exchanged with the server using sockets.
            </li>
        </ul>
</body>
</html>