# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## Name : Nandhika P

## Reg no : 212223040125

## PROGRAM

Client 
```
import socket
s=socket.socket()
s.connect(('localhost',8003))
while True:
    msg=input("client > ")
    s.send(msg.encode())
    print("server > ",s.recv(1024).decode())
```
Server
```
import socket
s=socket.socket()
s.bind(('localhost',8003))
s.listen(5)
c,addr=s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    print("cliet > ",clientMessage)
    msg=input("server > ")
    c.send(msg.encode())
 ```   
## OUPUT

Client

![image](https://github.com/user-attachments/assets/d5eee608-4b7f-4e5e-8b8d-12596c4bfb12)

server

![image](https://github.com/user-attachments/assets/819190d9-5306-4024-8ea2-b49d3743b8bc)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
