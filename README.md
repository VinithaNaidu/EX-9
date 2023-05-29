# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE :03-05-2023
## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server

4.Send and receive the message using the send function in socket.

# PROGRAM :
## CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER :
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
### OUTPUT :
## CLIENT :
![image](https://github.com/VinithaNaidu/EX-9/assets/121166004/6e1d7ee2-fb0f-4ade-980e-3e04599bf75b)


## SERVER :
![image](https://github.com/VinithaNaidu/EX-9/assets/121166004/9fee8b19-04c7-4f01-887e-2670d88e7f75)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
