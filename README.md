# Ex. 4 — Execution of Network Commands
# Name: Sanjeev Kumar
# Reg.No: 212224040290

## AIM:
Use of Network commands in Real Time environment

## Software: 
Command Prompt And Network Protocol Analyzer

## Procedure: 
To do this experiment, follow these steps:

## Networking Commands Experiment
This experiment involves understanding basic networking commands and configuring network devices. Below are the key topics covered:

### Basic Networking Commands
- **`cpdump`** - Capture and analyze network traffic.
- **`netstat`** - Display network connections, routing tables, and interface statistics.
- **`ifconfig`** - Display and configure network interfaces.
- **`nslookup`** - Query DNS records and troubleshoot DNS issues.
- **`traceroute`** - Trace the path packets take to a destination.

### Capturing PDU with a Network Protocol Analyzer
- Capture **ping** and **traceroute** Protocol Data Units (PDUs) using a network protocol analyzer.

### Router Configuration Commands
- **Switching to Privileged Mode**: Learn how to enter privileged mode on a router.
- **Switching to Normal Mode**: Return to normal user mode on the router.
- **Configuring Router Interface**: Commands to configure router interfaces and IP addressing.
- **Saving Configuration**: Save configurations to flash memory or permanent storage.

### Types of Commands
- **Configuring the Router**: Commands for setting up and managing the router.
- **General Network Configuration Commands**: Basic commands for network setup and troubleshooting.
- **Privileged Mode Commands**: Commands available in privileged mode for advanced configuration.
- **Router Processes & Statistics**: Monitoring and managing router processes and statistics.
- **IP Commands**: Commands related to configuring and troubleshooting IP settings.
- **Other IP Commands**: e.g., `show ip route` for displaying the router's routing table.


## PROGRAM:
Server:

    import socket 
    s=socket.socket() 
    s.connect(('localhost',8000)) 
    while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())

Client:

    import socket 
    from pythonping import ping 
    s=socket.socket() 
    s.bind(('localhost'8000)) 
    s.listen(5) 
    c,addr=s.accept() 
    while True: 
    hostname=c.recv(1024).decode() 
    try: 
    c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
    c.send("Not Found".encode())

TRACEROUTE COMMAND:

    from scapy.all import*     
    target = ["www.google.com"]     
    result, unans = traceroute(target,maxttl=32) 
    print(result,unans)

## Output
![image](https://github.com/user-attachments/assets/bc5c0ca0-8aaa-4d79-9c65-c994a77f5f12)
![image-2](https://github.com/user-attachments/assets/b13b0547-0d7f-42f0-80e2-a436a0b4b82b)



## Result
Thus Execution of Network commands Performed 
