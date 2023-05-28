# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :26-04-2023

# AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

# ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server.
4.Send and receive the message using the send function in socket.
```
# PROGRAM :
## CLIENT :
```
# Developed by: M.D.HARINI
# Register No: 212222230043
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER :
```
# Developed by: M.D.HARINI
# Register No: 212222230043
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
# OUTPUT :
## CLIENT :
![image](https://github.com/harinidq/EX-8/assets/113497680/a66f7fd5-aec6-42cc-bba3-53996ad063df)


## SERVER :
![image](https://github.com/harinidq/EX-8/assets/113497680/4b0a3dcf-ae33-460b-9821-656c252cd158)


# RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
