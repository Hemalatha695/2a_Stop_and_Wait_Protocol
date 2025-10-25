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
Client.py

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
## OUTPUT
<img width="976" height="380" alt="492606903-c303905d-fd84-4fee-9645-c7904f085844" src="https://github.com/user-attachments/assets/4bedf5db-40d1-41d4-a19b-0e1d259a91c7" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
