# 19CS406-EX-1 STUDY OF SOCKET PROGRAMMING WITH CLIENT-SERVER MODEL

## DATE : 08-03-2023

## AIM :
To write a python program to perform client server model.


## ALGORITHM :
Start the program. Get the frame size from the user To create the frame based on the user request. To send frames to server from the client side. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client. Stop the program.



## CLIENT PROGRAM :
```
\*
NAME : ABINAYA S
ROLL NO : 212222230002
import socket

s=socket.socket()

s.bind(('localhost',8080))

s.listen(5)

c,addr=s.accept()

while True:

i=input("ENter a data:")

c.send(i.encode())

ack=c.recv(1024).decode()

if ack:

	print(ack)

	continue

else:

	c.close()

	break
 ```
## SERVER PROGRAM :
```
import socket

s=socket.socket()

s.connect(('localhost',8080))

while True:

print(s.recv(1024).decode())

s.send("Recieved".encode())
```




## CLIENT OUTPUT :
![O1](https://github.com/LATHIKESHWARAN/19CS406-EX-1/assets/119393556/5a4f28ee-753d-44cb-a2bb-a76fba6bbb06)

## SERVER OUTPUT :
![O2](https://github.com/LATHIKESHWARAN/19CS406-EX-1/assets/119393556/aacb966e-f6b5-4968-8256-bb6542a954cd)




## RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.
