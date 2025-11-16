# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program
Client
```
import socket

from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5)
c,addr=s.accept()

while True:
    hostname=c.recv(1024).decode()
    try:
        c.send(str(ping(hostname, verbose=False)).encode())
    except KeyError:
        c.send("Not Found".encode())
```

Server
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    ip=input("Enter the website you want to ping ")
    s.send(ip.encode())
    print(s.recv(1024).decode())
```

## Output
## Client & Server
<img width="930" height="200" alt="image" src="https://github.com/user-attachments/assets/4bfa697d-a44d-4d41-b761-3772f10007b0" />

## netstat
<img width="745" height="288" alt="image" src="https://github.com/user-attachments/assets/dc444a48-ec9d-42c6-8323-1a82d0583ac3" />

## ipconfig
<img width="651" height="288" alt="image" src="https://github.com/user-attachments/assets/355bf7f8-fade-4854-a7b5-6b177f824bf5" />

## ping
<img width="713" height="292" alt="image" src="https://github.com/user-attachments/assets/e138e188-0721-4448-81d3-335d5e285e90" />

## tracert
<img width="656" height="278" alt="image" src="https://github.com/user-attachments/assets/5239e4f1-59b6-442e-8b2b-85206f4c923d" />

## nslookup
<img width="444" height="167" alt="image" src="https://github.com/user-attachments/assets/56afd050-7896-49dc-8d00-a8b24704debd" />

## getmac & hostname
<img width="715" height="219" alt="image" src="https://github.com/user-attachments/assets/9112f18e-b748-4231-9de8-4daeb9073bfd" />

## nbtstat
<img width="872" height="273" alt="image" src="https://github.com/user-attachments/assets/874baedf-dcfd-4c1e-8808-c64ad36e3830" />

## arp 
<img width="805" height="282" alt="image" src="https://github.com/user-attachments/assets/ba285551-2c27-42da-a89b-25d1c7809c5d" />

## systeminfo
<img width="720" height="267" alt="image" src="https://github.com/user-attachments/assets/8d8a613e-39da-4393-bd2d-4931529192f8" />



## Result
Thus Execution of Network commands Performed 
