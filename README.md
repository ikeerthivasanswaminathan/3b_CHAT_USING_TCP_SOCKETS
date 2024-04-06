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

![ex3bclient](https://github.com/ikeerthivasanswaminathan/3b_CHAT_USING_TCP_SOCKETS/assets/148937372/72551f2d-c8c5-4e10-9487-e759813a3bbb)

Server

![ex3bserver](https://github.com/ikeerthivasanswaminathan/3b_CHAT_USING_TCP_SOCKETS/assets/148937372/ccdde630-90f8-4316-be59-da19728bced7)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
