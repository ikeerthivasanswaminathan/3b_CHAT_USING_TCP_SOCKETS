# 3b.CREATION FOR CHAT USING TCP SOCKETS

## AIM
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server.
4. Send and receive the message using the send function in socket.

## PROGRAM

client.py

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```

server.py

```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```

## OUPUT

Client

![ex3bclient (new)](https://github.com/ikeerthivasanswaminathan/3b_CHAT_USING_TCP_SOCKETS/assets/148937372/75ccf079-5c28-452b-8be8-5c596ac1b161)

Server

![ex3bserver (new)](https://github.com/ikeerthivasanswaminathan/3b_CHAT_USING_TCP_SOCKETS/assets/148937372/0e6ad9f7-ce47-4a5f-9ab4-60c72952b201)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
