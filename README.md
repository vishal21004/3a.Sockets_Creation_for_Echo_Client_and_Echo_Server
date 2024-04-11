## REG NO : 212222230177
## NAME : VISHAL M.A
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
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT:
## CLIENT:
![clnt](https://github.com/vishal21004/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119560110/04f9a06f-8dfc-421b-acf6-cf43016c07ae)

## SERVER:
![srvr](https://github.com/vishal21004/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119560110/59b16e8b-7b14-4ab6-8ade-b60ef4d75397)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
