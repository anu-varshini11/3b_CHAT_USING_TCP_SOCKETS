# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
client
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
	msg=input("Client > ")
	s.send(msg.encode())
	print("Server > ",s.recv(1024).decode())
```
```
server
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
	ClientMessage=c.recv(1024).decode()
	print("Client > ",ClientMessage)
	msg=input("Sever > ")
	c.send(msg.encode())
```
## OUPUT
![Screenshot from 2024-10-22 09-17-18](https://github.com/user-attachments/assets/920804b3-6a34-4041-a154-1697b1499732)

![Screenshot from 2024-10-22 09-17-23](https://github.com/user-attachments/assets/dd2b8dcd-365d-43fd-ba4c-4229d0a3cd77)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
