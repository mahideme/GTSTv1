
# Scanning
system hacking/host/website scanning
finding for vulnerability(weakness)

- The 2nd phase of Ethical Hacking. 
- It is the step which **helps to test a system based on the information we gathered**. 
- Scanning is another essential step, which is necessary, and it refers to the **package of techniques or procedures used to identify hosts, ports, and various services within a system.**
- try to gather **more information**. but test yetederegu information new minoren or we test what we got
- we gather information mostly in **active** way. and detail about specific information(host, port..)

# Why do we do scanning? 
- It helps to **Identify HOST’s System detail** 
     - Operation System 
     - Service versions 
- To **Discover Open Ports** 
- To **Discover Live Systems**

many scanning 
# Network Scanning 
system web lay metekem enchlalen, yerasachew scanningm alachew  beye fildu

- This is a method of **Scanning a network** and **getting more information.** 
- There are Many kinds of **scanning methods and tools** **for different purpose**. 
      - For Network mainly: NMAP, netdiscovery 
      - For Subdomain: Sublist3r,subfinder,amass 
      - For website: Nuclei , Nessus, Acunitix


# Nmap - Network Mapper 
- is A network scanning and exploring tool **used by network and security experts**
- It is **used to scan Network ,Ports, OS**,... 
- It is made for windows and Linux 
- ON kali Linux it is built in. 
- To check the existence of nmap on your system 
      - nmap --version

### Live System Discovery 
to hack by using ip address is possible when we get **website ip address(because they have static ip address).**

- Discovering live system means, **Checking up** and **running hosts(clients/servers) on a network.**
- We have seen **Host checking** last time **with ping sweep method**.(**getting ip with link**)  But How does the ping worked?

#### Ping Sweep 
- This is **a method of checking if host is up or down.** 
- It **uses ==ICMP==(Internet Control Message Protocol) packets for checking purpose**
- It **sends Echo request** and **waits** for response **if there is Echo reply** then that **system is up!**

       - With ping sweep 
       --From echo requests we can gather the following informations 
              - OS type 
                  - Windows ( 32 byte )
                    - ttl=108 
                  - Linux ( 64 byte ) 
                    - ttl=64 - Connection stability 
        - Time Ttl : time to live

#### Nmap ping sweep 
- Nmap can perform ping sweep too. 
    - Syntax: 
        - ==nmap -sn IP==        -sn = no port sc
- also used to scan any website
     - nmap google.com
     - nmap scanme.nmap.


● -> What do we do ,to know all the hosts on our system? ● ping can take 1 host only?? ● Nmap can scan the whole range. ● Guess how? ● You can do the ping sweep with little modification on the IP ● Syntax: ○ nmap -sn GatewayIP-255 ○ nmap -sn GatewayIP/networkBits(subnet mask) - CIDR notation ■ Network bits depend on the IP Class. ● This will not work on Virtual machines network.

warning 1

warning2
warning++ ● Some Organizations or system admins, will block any ICMP requests ● Here the ping sweep wont work, and when you try this it says “host is down” but it is not ● To make it work we just escape the some option ● Syntax: ○ nmap -Pn IP ● This method will Jump host discovery because it will take the ip as Up and try to do port discoveries




