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
client.echo
```
import socket 
s = socket.socket()
s.connect(('localhost', 8080))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
 ```
server.echo
```
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUPUT
client.echo

<img width="1318" height="317" alt="Screenshot 2026-11-18 085627" src="https://github.com/user-attachments/assets/72a69071-168d-42a7-9dd4-0907033f1805" />

server.echo

<img width="1318" height="281" alt="Screenshot 2026-11-18 085635" src="https://github.com/user-attachments/assets/99b642d4-b9d8-48a0-9169-2ada89e69012" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
