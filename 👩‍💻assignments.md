
1. Write a port scanner without using nmap python module  
2. Write a port scanner tool using nmap module. Py  
3. Read about nmap module ( there will be question )  
4. Write a host discovery tool in python you will determine the gateway ip and the IP class   
5. Write a tool in bash that accepts IP, and NSE script name then it will run nmap scan.

```python

import socket 
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM) socket.setdefaulttimeout(1) 
host = input("[*] Enter your target IP: ") 
def portscanner(port): 
    try: 
        sock.connect((host, port)) 
        print(f"[+] Port {port} is opened") 
    except: 
        print(f"[!!] Port {port} is closed") 
for port in range(1, 10):
    portscanner(port)

```


```python

import nmap 
target = input("Enter the IP address to scan: ") 
scanner = nmap.PortScanner() 
for i in range(1,11): 
    result = scanner.scan(target, str(i)) 
    try: 
        result = result['scan'][target]['tcp'][str(i)]['state'] 
        print(f'port {i} is {result}.')
    except KeyError: 
        print(f'port {i} is not open')
```


```python

def get_cidr_notation(ip_class):
    if ip_class == "A": 
        return "/8" 
    elif ip_class == "B": 
        return "/16" 
    elif ip_class == "C": 
        return "/24" 
    else: 
        return "Invalid IP class Use A, B, or C." 
if __name__ == "__main__": 
    ip_address = input("Enter the IP address: ") 
    ip_class = input("Enter the IP class (A, B, or C): ") 
    cidr_notation = get_cidr_notation(ip_class) 
    print(f"CIDR notation: {cidr_notation}")
```


```bash

#!/bin/bash
IP="$1"
NSE_SCRIPT="$2" 
nmap -sV -p 1-65535 --script "$NSE_SCRIPT" "$IP"
```