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
client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8002)) 
while True: 
     msg=input("Client > ") 
     s.send(msg.encode()) 
     print("Server > ",s.recv(1024).decode())

```


server
```
import socket 
s=socket.socket() 
s.bind(('localhost',8002)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
             ClientMessage=c.recv(1024).decode() 
             print("Client > ",ClientMessage) 
             msg=input("Server > ") 
             c.send(msg.encode()) 

```

## OUPUT
![Screenshot 2025-05-09 093107](https://github.com/user-attachments/assets/eb101518-5f93-4f70-b6b1-4f273b4db84a)


![image](https://github.com/user-attachments/assets/5779c97c-59c9-408a-aab7-933f028b20fb)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
