# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME: ZAFREEN J
## REGISTER NO:212223040252
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
CLIENT.PY

```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    c.send((clientMessage.encode()))



```
SERVER.PY
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())

```
## OUPUT

CLIENT.PY


![Screenshot 2024-04-27 184350](https://github.com/ZafreenJagir/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870573/08e70951-9936-4e5c-bcae-502a22d5ccb5)



SERVER.PY

![Screenshot 2024-04-27 184340](https://github.com/ZafreenJagir/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870573/d3e393e7-6965-45ee-9cfb-af5329524663)



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
