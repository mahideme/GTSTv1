

==**Backtrack**== is the previous name of kali Linux.


# 📦Menu

1. Information gathering
    Common Tools in system, network, host.
     - maltego, nmap, recon-ng
2. vulnerability Analysis
    common tools for finding vulnerabilities.
     -  nikto, nmap
3. Web Application Analysis
   Common Tools for Finding Vulnerabilities and exploits on websites.
     - burpsuite, sqlmap, wpscan, ZAP
 4. Database Assessment
    Common Tools for Finding Vulnerabilities and exploits on Databases.
      - JAQL injection, sqlmap
5.  Password Attacks
    Common Tools for exploiting Passwords for login, websites, application, windows..
      - hashcat, john, 
6. Wireless Attacks 
    Common Tools for exploiting Wireless Systems like wifi, bluetooth..
    - aircrack-ng, wifite, reaver
7. Reverse Engineering 
    Common Tools for exploiting Softwares, Mobile Applications and any binary files.
      - apktool, ghidra
8. Exploitation Tools
    Common Tools for exploiting Softwares, Mobile ,Computers ,websites and any things. use to gain access
      - metasploit
9. Sniffing & Spoofing 
    Common Tools for Listening or hijacking networks
      - wireshark
10. POST exploitation 
    Common Tools for Maintaining our access. Used after exploiting a system
    - backdoor
11. Forensics
    Common Tools for Doing researches and investigate a Cyber Attacks.
     - hashdeep
12. Reporting tools 
    Common Tools for Report preparation. After some forensic you will get data and you will write report and these tools will help you.
     - recordmydisk
13. Social Engineering tools 
    Common Tools Used for Social Engineering attacks
     - maltego, backdoor
14. System Services 
    Common Buttons used to start some services
      - beef start, beef stop, dradis start, dradis stop
15. Usually used applications 
    Common Softwares for some basic purposes.


# 📃Linux Commands

- Linux Systems uses shell(Terminal). The shell help us **to Communicate with the kernel** and helps **to execute codes.**
## ⬛the shell

- terminal have 5 parts
      - username =  user of the machine
      - hostname  = machine name
      - current directory =path 
      - priviledge =$ - user, # - root
      - command place = __
- home directory is " ~ " = tilda
- local directory with " . " 
- all directory " * "

tilda - current directory home directory

## 🏹commands

- ls  --  List Directory 
     -- ls -l 
     -- ls -a 
     -- ls filename 
     -- ls -R => recursive
     -- You can combine them, ls -Rla 
     -- Linux hidden files start with dot
-  cd -- Change Directory 
     --SYNOPSIS cd [directory]. it is used to change current working directory.
     -- cd / => root 
     -- cd => home 
     -- cd .. => 1x Back 
     -- cd ../.. => 2x Back 
     -- cd foldername ( for space name "folder name")
 -  Pwd -- print working directory 
      -- SYNOPSIS pwd [-options]. It prints the path of the working directory, starting from the root.
  - echo  SYNOPSIS echo [option] [string]. 
       -- echo command in linux is used to display line of text/string that are passed as an argument . This is a built in command that is mostly used in shell scripts and batch files to output status text to the screen or a file.
       -- You can write texts into files. ○ echo text > file.txt ● You can add texts(append) ○ echo text >> file.txt
   - cat / head / tail / less -- SYNOPSIS cat [FILE]...
      -- Used to show the content of a file
  - touch -- SYNOPSIS touch [FILE1] [FILE2] [FILE3] 
        -- Creates any kind of Files with the name you gave it. With empty inside
     
- Mkdir -- make directory
        --SYNOPSIS mkdir [FOLDER-NAME1] [FOLDER-NAME2] [FOLDER-NAME3]
        --Creates Folder with the name u gave it. - DON’T forget to add the “ “ when you are using folders with space between them. 
- clear --  SYNOPSIS clear 
      -- Clears your screen
- grep - global search for regular expression 
        -- grep [options] pattern [files] 
        --The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for global search for regular expression and print out). 
        - grep -i “search” file 
             - case insensitive 
        - grep -c “search” file 
             - count numbers 
        - grep -l “search” * 
            - displays filename 
	    - grep -R “search” foldername 
	          - search text in folders 
	    - grep -v ‘term’ filename 
	         - To display without this term 
	    - grep -n “term” file 
	         - To display the term find number

- Wc - word count 
      -- SYNOPSIS wc [OPTION]... [FILE]... 
      -- It is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments. 
      --Line(-l) word(-w) byte(-c)

#### 📎Multiple Command Executions 
- run/ execute multiple commands in 1 line.
- 3 methods: 
- And ( && )
    -  All commands you entered will be executed. If both are working without error
- Or ( || )
     - On OR operation the command will be executed. If it have error or not 

- Pipeing( | )
     - On pipe, will help you run commands by using the output of the 1st command as the input for the next one


### 📎other commands that are common

1. ln - Create symbolic links (shortcuts) to other files
2. less - Linux command to display paged outputs in the terminal
3. man - Access manual pages for all Linux command
4. uname - Linux command to get basic information about the OS
5. whoami - Get the active username
6. tar - Command to extract and compress files in linux
7. grep - Search for a string within an output
8. head - Return the specified number of lines from the top
9. tail - Return the specified number of lines from the bottom
10. diff - Find the difference between two files
11. cmp - Allows you to check if two files are identical
12. comm - Combines the functionality of diff and cmp
13. sort - Linux command to sort the content of a file while outputting
14. export - Export environment variables in Linux 
15. zip - Zip files in Linux 
16. unzip - Unzip files in Linux 
17. ssh - Secure Shell command in Linux 
18. service - Linux command to start and stop services 
19. ps - Display active processes 
20. kill and killall - Kill active processes by process ID or name
21. df - Display disk filesystem information 
22. mount - Mount file systems in Linux
23. chmod - Command to change file permissions
24. chown - Command for granting ownership of files or folders 
25. ifconfig - Display network interfaces and IP addresses 
26. traceroute - Trace all the network hops to reach the destination
27. wget - Direct download files from the internet 
28. ufw - Firewall command 
29. iptables - Base firewall for all other firewall utilities to interface with 
30. apt, pacman, yum, rpm - Package managers depending on the distribution 
31. sudo - Command to escalate privileges in Linux
32. cal - View a command-line calendar 
33. alias - Create custom shortcuts for your regularly used command 
34. dd - Majorly used for creating bootable USB sticks 
35. whereis - Locate the binary, source, and manual pages for a command 
36. whatis - Find what a command is used for 
37. top - View active processes live with their system usage
38. useradd and usermod - Add a new user or change existing user data
39. passwd - Create or update passwords for existing users

### 😍100 Essential Kali Linux Commands for Penetration Testing and Ethical Hacking

1. `ifconfig` - Display network interfaces and their configurations.
2. `ping` - Send ICMP echo requests to a target host.
3. `netstat` - Display network statistics (connections, listening ports, etc.).
4. `nmap` - Perform network scanning and port enumeration.
5. `arp` - Display or modify the ARP cache.
6. `dig` - Perform DNS queries.
7. `whois` - Retrieve WHOIS information for a domain.
8. `host` - Perform DNS lookups.
9. `traceroute` - Display the route packets take to a destination.
10. `route` - Show or manipulate the IP routing table.
11. `iptables` - Configure firewall rules.
12. `tcpdump` - Capture and analyze network traffic.
13. `wireshark` - Graphical packet capture and analysis tool.
14. `ssh` - Securely connect to remote systems.
15. `nc` - Netcat - a versatile networking utility for testing.
16. `metasploit` - Framework for developing and executing exploits.
17. `hydra` - Brute-force login attacks.
18. `john` - Password cracking tool.
19. `aircrack-ng` - Wireless network security assessment tool.
20. `reaver` - Brute-force attacks against WPS-enabled routers.
21. `sqlmap` - Automated SQL injection and database takeover tool.
22. `enum4linux` - Enumerate information from Windows and Samba systems.
23. `nikto` - Web server vulnerability scanner.
24. `dirb` - Web content scanner.
25. `wpscan` - WordPress vulnerability scanner.
26. `burp` - Web application security testing tool.
27. `sqlninja` - SQL server injection and takeover tool.
28. `ettercap` - Man-in-the-middle attack tool.
29. `snort` - Network intrusion detection system.
30. `openvas` - Open Vulnerability Assessment System.
31. `armitage` - Graphical user interface for Metasploit.
32. `xsser` - Cross-Site Scripting (XSS) exploitation tool.
33. `dirbuster` - Directory and file brute-forcing tool.
34. `hashcat` - Advanced password recovery tool.
35. `volatility` - Memory forensics tool.
36. `autopsy` - Digital forensics platform.
37. `gobuster` - Directory and file brute-forcing tool.
38. `dnsrecon` - DNS enumeration tool.
39. `steghide` - Hide data inside image and audio files.
40. `stegcracker` - Steganography brute-force tool.
41. `sshuttle` - VPN-like tunneling tool.
42. `mitmproxy` - Intercept and modify HTTP/HTTPS traffic.
43. `hash-identifier` - Identify hash types.
44. `samdump2` - Extract password hashes from Windows SAM files.
45. `radare2` - Reverse engineering framework.
46. `airgeddon` - Wireless auditing framework.
47. `mitm6` - Man-in-the-middle attack tool for IPv6.
48. `mitmAP` - Create fake access points for man-in-the-middle attacks.
49. `dmitry` - Intelligence gathering tool.
50. `theharvester` - Gather information from public sources.
51. `exiftool` - Read and write metadata in files.
52. `binwalk` -Analyze and extract files from binary images.
53. `foremost` - File carving tool.
54. `scalpel` - File carving and recovery tool.
55. `ssh-keygen` - Generate SSH key pairs.
56. `john` - Password cracker (John the Ripper).
57. `tcpflow` - Capture and analyze TCP connections.
58. `davtest` - Test WebDAV-enabled servers.
59. `sslscan` - SSL/TLS vulnerability scanner.
60. `wifite` - Automated wireless network auditing tool.
61. `tshark` - Command-line Wireshark.
62. `macchanger` - Change MAC address.
63. `nbtscan` - NetBIOS scanner.
64. `ike-scan` - VPN fingerprinting and testing tool.
65. `hashcat-utils` - Additional utilities for hashcat.
66. `veil` - Generate undetectable payload encoders.
67. `bettercap` - Man-in-the-middle framework.
68. `ferret` - Network data sniffing tool.
69. `maltego` - Open-source intelligence and forensics tool.
70. `pdf-parser` - Analyze PDF documents.
71. `openvpn` - VPN server and client.
72. `msfvenom` - Payload generation tool for Metasploit.
73. `dnsenum` - DNS enumeration tool.
74. `p0f` - Passive OS fingerprinting tool.
75. `thc-ipv6` - IPv6 attack toolkit.
76. `chntpw` - Change or blank Windows passwords.
77. `pcredz` - Extract Windows credentials from memory dumps.
78. `exploitdb` - Exploit database for Metasploit.
79. `dmitry` - Information gathering tool.
80. `yara` - Pattern matching swiss knife.
81. `db_nmap` - Use Nmap from the Metasploit framework.
82. `msfpc` - Generate Metasploit payloads.
83. `mac-robber` - Collect MAC timestamps from files and directories.
84. `enumiax` - Enumerate information from Asterisk PBX systems.
85. `ipcalc` - Calculate IP network parameters.
86. `mimikatz` - Extract Windows credentials from memory.
87. `wifiphisher` - Automated Wi-Fi phishing tool.
88. `metagoofil` - Gather metadata from public documents.
89. `recon-ng` - Web reconnaissance framework.
90. `exploitdb` - Searchable exploit database.
91. `enumiax` - Enumerate information from Asterisk PBX systems.
92. `golismero` - Web application security testing framework.
93. `sparta` - GUI-based network infrastructure penetration testing tool.
94. `ike-scan` - VPN fingerprinting and testing tool.
95. `nmapsi4` - Nmap graphical interface.
96. `socat` - Multipurpose relay for bidirectional data transfer.
97. `dirbuster-ng` - Directory and file brute-forcing tool.
98. `davtest` - Test WebDAV-enabled servers.
99. `udis86` - Disassembler library for x86 and x86-64.
100. `lynis` - Security auditing tool.


---

# 🎉End of day three 🎉
NEXT -- [[💖Day4_Further on Linux]]