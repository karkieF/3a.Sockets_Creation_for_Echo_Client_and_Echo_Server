# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### client.py:
```
import socket
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py:
```
import socket
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage)  
    c.send(ClientMessage.encode())
```
## OUPUT
### client.py:
<img width="163" height="204" alt="image" src="https://github.com/user-attachments/assets/d472bd4c-fda1-4727-b57b-6caf157dd391" />

### server.py:
<img width="179" height="88" alt="image" src="https://github.com/user-attachments/assets/02cfa404-f1c4-4159-a6e7-670e3845cccb" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
