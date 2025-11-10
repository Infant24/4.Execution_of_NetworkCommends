# 4.Execution_of_NetworkCommands

## AIM:
Use of Network commands in Real Time environment.

## Software : 
Command Prompt And Network Protocol Analyzer.

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

## PROGRAM:

## SERVER:

```
import socket
from pythonping import ping s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True:
hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```

## CLIENT:

```
import socket s=socket.socket() s.connect(('localhost',8000)) 
while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode()) print(s.recv(1024).decode())

```
## TRANCEROUTE COMMAND

```
from scapy.all import* target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32) print(result,unans)
```

## Output:

## CLIENT:

<img width="873" height="233" alt="image" src="https://github.com/user-attachments/assets/e416fe99-7e59-4d1f-b729-95310f9c1681" />

## SERVER:

<img width="877" height="482" alt="image" src="https://github.com/user-attachments/assets/f4c16642-d7b0-48f5-baa0-fd1c7c0f2a34" />

## TRANCEROUTE COMMAND:

<img width="874" height="331" alt="image" src="https://github.com/user-attachments/assets/312cb98e-49ab-4750-82c8-60498608062d" />

## Result:

Thus Execution of Network commands Performed 
