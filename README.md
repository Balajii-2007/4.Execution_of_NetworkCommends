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
```
client.py
import socket
from pythonping import ping
s=socket.socket() s.bind(('localhost'8000)) s.listen(5) c,addr=s.accept()
while True: hostname=c.recv(1024).decode() try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```
```
server.py

import socket s=socket.socket() s.connect(('localhost',8000)) while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```

## Output
NETSTAT
<img width="1033" height="747" alt="image" src="https://github.com/user-attachments/assets/df0b6dc4-0488-4478-b494-f7cb7959da99" />

IP CONFIG
<img width="937" height="862" alt="image" src="https://github.com/user-attachments/assets/7e541a5a-0bba-4067-bc82-51b3a5aa4b9b" />

GETMAC
<img width="1012" height="192" alt="image" src="https://github.com/user-attachments/assets/07428e9a-d6c0-44db-8839-bc700d4d13a0" />

ARP
<img width="1048" height="797" alt="image" src="https://github.com/user-attachments/assets/fee31d5b-a2e4-4ac6-8d6b-b4368e7bc2f8" />

SYSTEM INFO
<img width="977" height="952" alt="image" src="https://github.com/user-attachments/assets/a4fb48e2-554b-4913-b220-e3ebb855ceb7" />

NBTSTAT
<img width="1027" height="608" alt="image" src="https://github.com/user-attachments/assets/6659fad6-990f-42a4-85f9-915912bc2e8e" />

HOSTNAME

<img width="389" height="86" alt="Screenshot 2026-05-19 130116" src="https://github.com/user-attachments/assets/315f9e94-614b-41ba-a216-fbc07262f16d" />

NS LOOKUP

<img width="452" height="123" alt="image" src="https://github.com/user-attachments/assets/c45d3e70-2189-4237-8b85-a0780bfe9035" />

PING

<img width="1097" height="807" alt="image" src="https://github.com/user-attachments/assets/e705a4dc-30fd-435b-a342-6ed42f811853" />

TRACET

<img width="936" height="108" alt="image" src="https://github.com/user-attachments/assets/1f0dbc1e-8cdf-4204-b72a-24d854435e63" />

## Result
Thus Execution of Network commands Performed 
