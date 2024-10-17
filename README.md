# 2a_Stop_and_Wait_Protocol
### Date:
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
#### RAMYA R
#### Reister Number: 21223230169
### Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()

   break
```
### Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT
![Screenshot 2024-10-17 124422](https://github.com/user-attachments/assets/85359a1a-97c3-4c8a-a070-00d325e897d7)

![Screenshot 2024-10-17 124410](https://github.com/user-attachments/assets/fd504069-edc1-4a45-95ef-8797d0655f7c)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

