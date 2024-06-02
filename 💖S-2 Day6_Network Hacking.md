
# Network Hacking 
- Network Hacking is gathering and exploiting of networks. 
- The networks can be WAN or LAN. 
- Network Hacking is an **offensive branch of computer security** related to networks hacking and the penetration of a target via the networking services or equipment. 
- This includes 
     - Network information gathering  -- tools - ping, traceroute
     - Sniffing -- process of monitoring and capturing all the  packets passing through a given network using  sniffing tools.
     - Network Attacks

## types of sniffing

1. passive sniffing - the traffic is visible but it is not altered in any way.     
               -  allows listening only
               - works with hub devices. - the traffic is sent to all the ports. so all hosts on the network can see the traffic. therefore an attacker can easily capture traffic going through.
               - now a days hub is not mostly used 
2. active sniffing - the traffic is not only monitored, but it may also be altered in some way as determined by the attack 
               - used to sniff a switch based network
        

### wireshark
	- a program to sniff the network
	- passive monitoring tool
	- protocol analyzer, but it uses only passive observation of network traffic
	- supports both live and offline analysis
	- it can capture and record network traffics and save it in form of cap/pcap file
#### tshark
-  command line tool like the wireshark it can capture
#### tcpdump 
- powerfull command line packet analyzer tool that captures and displays network packets transmitted and received over a network interface
- sudo tcpdump -i --interface--



#  ARP/Address Resolution protocol/
- mapping dynamic ip address to permanent physical machin address(MAC) in a LAN
- reason- because computers need to know both the ip address and the mac address of a destination before they can start network communication.


# mac flooding
- attack on switch
- mac table - has port and mac address
- this flooding is by giving a lot of feck mac address and then the correct mac address will be out from the table.
- prevention
      - port security -- limit the number of mac address from one device 
      - mac filtering --  ban the computer 

# ARP spoof
- acting as a router
- man in the middle attack