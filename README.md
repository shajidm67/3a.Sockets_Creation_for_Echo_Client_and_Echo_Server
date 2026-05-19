# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## REF NO:25015705
### DATE:12-02-2026
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
server.py
~~~
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
~~~
client.py
~~~
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~
## OUTPUT
server
<img width="1300" height="1078" alt="Screenshot 2026-02-11 111525" src="https://github.com/user-attachments/assets/aa9381e1-d6ad-4052-bcad-11eae6de3c6e" />

client
<img width="1532" height="1041" alt="Screenshot 2026-02-11 111716" src="https://github.com/user-attachments/assets/f10deb56-0d37-4c2a-bc7e-12b199532802" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
