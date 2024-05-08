# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# NAME : DHARANISH MS
# REGISTER NO : 212223240027
## AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT 
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())
```
### SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT
### CLIENT
![CLIENT 3A](https://github.com/MSDharanish-23011819/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147139454/c264b083-2cd7-4ac3-980a-42f73e9e0e4d)

### SERVER
![SERVER 3A](https://github.com/MSDharanish-23011819/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147139454/668a6f29-796b-41aa-9df0-72cd22c015a8)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
