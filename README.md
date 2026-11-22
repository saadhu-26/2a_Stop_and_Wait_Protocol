# 2a_Stop_and_Wait_Protocol

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
```
client side:
  i=input("Enter a data: ") 
  c.send(i.encode()) 
  ack=c.recv(1024).decode() 
  if ack: 
    print(ack) 
    continue 
  else: 
    c.close() 
    break

server side:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
  print(s.recv(1024).decode()) 
  s.send("Acknowledgement Recived".encode())
```
## OUTPUT

<img width="658" height="264" alt="image" src="https://github.com/user-attachments/assets/a2a3b9f4-4277-4dac-a2dd-f111dc1af271" />

<img width="631" height="174" alt="image" src="https://github.com/user-attachments/assets/52c160b8-6db4-4dca-9084-9903f093c4cb" />

## RESULT

Thus, python program to perform stop and wait protocol was successfully executed.
