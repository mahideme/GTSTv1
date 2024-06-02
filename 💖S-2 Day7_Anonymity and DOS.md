
# Anonymity

- Keeping your **identity** private, **but not your actions**.  
     - For example, using a fake name to post messages to a social media platform. fake personality - fake mac address, ip address, computer name, 
- Anonymity is Simply using a **fake Profile/Location/Identity/personality**.


## online privacy

- incognito/privacy tabs
     - These Programs are simply not logging what we are doing(aka history, cache, cookie) but still the site we visit with this program will have our ip and other information also our ISP/internet service provider/ will know. 
     - Therefore, they don't give as real privacy


## Methods of Anonymity 
- There are several ways to be protected or to be Anonymous on the internet. 
- These methods can change our identity, location or personality. 
### 1. Proxy-chains
intermediary 

- A proxy server is a system or router that provides a gateway between users and the internet. 
     - Therefore, it helps prevent cyber attackers from entering a private network. but if proxy is asked it tells what that ip was. so to handle this - they created chain
- Proxy chain is simply a chain of proxys. 
    - We have a lot of proxy lists so our request will pass through lot of proxys. 
    - This will hide our IP for a long time safe

#### Types of ProxyChains 
Based on the path we follow 
- There are 4 Types of proxychains. 
    1. Dynamic chain - the way the proxy servers are chained is as the proxy list given. 

          - ==skipped== if  one proxy is **not working server**
          - ==display error== if **all doesn't work**
    
    2. Strict Chain 
          -  ==display error== if **one server is not working**
    3. Round Robin Chain 
         - ==skip== if **1 proxy is not working** 
         - ==start again and check them== if **all the proxies not working**
        
    4. Random Chain - choose some proxy server randomly and creates chain in random order.
         - ==skipped== for **not working **
         - request will be in random sequence of servers

where do we get proxy server
- we can create - 
- paid proxy servers
- government sponsored 
- Find some Proxy servers to use. 
    -  google.com 
    -  https://geonode.com/
- /etc/proxychains4.conf
- fill based on what we want and save it
- then to request 
- to be anonymous on active footprinting time we use proxychains command 
     - proxychins curl if config.me




### 2. Tor Network - the onion routing 
- open source privacy network 
- enables anonymous web browsing
- uses secure, encrypted protocols to ensure users online privacy is protected. 
- uses node - computer that join the tor network 
     -  entry, relay/bridge and exit not
     - 3 times encryption from the the entry on each layer their will be one decrypt 
     - d/f with proxy is its encryption technique
         - before sending to the destination there is  3 encryption 
         - how they encrypt
            - when we get tor network we get each layer's  3 or 4 entry and relay node and exit node and also public key to encrypt what we send.
        - to access the entry node - tor uses proxy - our local host
             - by default tor uses our computer ip , port(9050), 127- local host
             - so to be unknown we use proxychains command
- When you use the Tor browser to digitally communicate or access a website, the Tor network does not directly connect your computer to that website. 
- Instead, the traffic from your browser is intercepted by Tor and bounced to a random number of other Tor users’ computers before passing the request to its final website destination.





### 3. VPN / virtual private network

- establishes a secure, encrypted connection between your  computer and internet, providing a private tunnel for your data and communications while you use public networks
- it also server like proxy but d/f with its encryption-
     - creates tunnel -- any attacker and government can't see what we sent
         - how government couldn't see
             - you -- isp -- internet -- vpn -- websites

#### Types of VPN 
A) ==SITE to SITE== 
- This is most commonly used **to join company networks together over the Internet** 
- allowing **multiple locations to communicate over the Internet as if they were local**. 
- Router + Routers -- vpn is set up on a router
- private networkachew ping endiderareg

B) ==Remote Access VPN== 
- involves the **client's computer creating a virtual interface that behaves as if it is on a client's network** 
    - Hacking game utilizes `OpenVPN`, which makes a TUN Adapter letting us access the labs 
- When analyzing these VPNs, an important piece to consider is the routing table that is created when joining the VPN. 
- If the **VPN only creates routes for specific networks** (ex: 10.10.10.0/24), this is called a `Split-Tunnel VPN` -- one way-- meaning i can access remotely access the network on that which i created connection via vpn  but  they can't access my neighbor networks they can access my network only, meaning the Internet connection is not going out of the VPN. - This is great for Hacking Games because it provides access to the Lab without the privacy concern of monitoring your internet connection. 

C) ==SSL VPN==
- essentially a **VPN that is done within our web browser** and is becoming increasingly common as web browsers are becoming capable of doing anything.
- These will stream applications or entire desktop sessions to your web browser.

-- ------- -              --      ---------- 
         the above's are ip hiders, fake ip generators
--------- --------------------------------------- 
         below are mac hider, computer hider, fake mac address
----- -----------

### 4. Mac change 

- sudo ifconfig "NIC" down
- sudo macchanger -r 'NIC'  -- give fake mac address automatically
- sudo ifconfig 'NIC' up
- macchanger -s 'NIC'  -- status
- sudo macchanger -m 'mac address' 'NIC'  -- to give mac address  manually
- macchanger -l  -- list of mac address list


### 5. Incognito
- This is a mode that browsers have. 
- This will help you to have a browser with out logging your history, cookies, cache,.. 
- This will help you when you are try to surf some site but if you dont need the site to know your identity, you can use this because it doesnt have any recording process.



### 6. Secured OS 
- This are Operating systems, that have a security and privacy feature. 
- Windows and Mac OS will record some of your activity also they are not good on privacy and security. 
- There for the always Best OS Linux is always recommended when you think about privacy and Security


### 7. Temp mail 
- https://temp-mail.org/

### 8. Temp number



## True anonymity is hard

- Achieving true anonymity on the internet requires good operational security (OPSEC) on your part to ensure your real IP address is not revealed.
- **Tools** that can hide your IP address and protect anonymity include **VPNs and the Tor anonymity network**, but **there’s no solution that can guarantee 100% anonymity.** **Tor** is sometimes considered to be **more anonymous than VPNs due to its decentralized nature,** but **it comes at the cost of lower performance, ease of use, and stability**


# internet web
classified into 3
surface web -- anything on search engine
deep web -- 
dark web
# Deep web 
- The deep web refers to **all the web pages and data that are not indexed by search engines and cannot be accessed through traditional search methods**. It **includes content that is protected by passwords, databases, and other security measures.** 
- Examples of deep web content include **private email accounts**, **online banking portals**, **subscription-based websites**, and more. 
- Essentially, the deep web is the part of the internet that **is not easily accessible to the general public.**
- we can do our website to be not searched by google and accessed on surface web -- when we configure website we can create a file that is called ==robots.txt== 

# DARK WEB 
- The dark web is a part of the internet that **isn't indexed by search engines.** 
- The dark web is a ***small portion of the deep web that is*** **intentionally hidden and requires specific software or configurations to access**. 
- It is **unique type of internet world.** 
- Their link ends with ==.onion== , this is because it **uses TOR networks**. 
- Also this kinds of **links won’t be opened by normal browser**. 
- For this purpose **we need a special .onion reading browser**, 
    - Example: **Tor browser**. 
- Many kinds of websites are there. 
     - You can buy credit card numbers, all manner of drugs, guns, counterfeit money, stolen subscription credentials, hacked Netflix accounts and software that helps you break into other people’s computers. 
     - Buy login credentials to a $50,000 Bank of America account, counterfeit $20 bills, prepaid debit cards, or a “lifetime” Netflix premium account. 
     - You can hire hackers to attack computers for you. You can buy usernames and passwords.
- Also there are emailing service sites and normal facebook too(but more secured). 
- As you see This side of internet is little bit dangerous because a lot of evil hackers are there. 
- For this purpose we have to change our identity, so we use Anonymity. 
- ALSO REMEMBER YOUR ISP WONT ALLOW YOU TO ACCESS IT.


There are Specific OS that are planned and Made for darkweb access. 
- Like linux based os on live boot, - **Tails OS - Whonix OS - Qube OS **
- We can use these OS for more Anonymity, but still the dark web sites are not easy to find. 
- Also TOR browser is so slow, based on your internet speed, it might not show you the correct result.
- thehidden.wiki -- to get onion links together
- there is email called -- ==proton mail==


# DOS and DDOS - Distributed Denial-of-Service Attacks

- used to crash a website by overwhelming the network with access requests from a computer. This method also crashes a targeted website and makes it unavailable to legitimate users.(like Mac spoofing) 
- It is purposeful attack
- On DDOS, the request will be sent from DIfferent Computers/hosts this will make the attack harder. 
- ==IT is Highly illegal!== 
- Techniques: 
    - SYN floods 
        - Sending lots of SYN 
    - Service Request floods 
         - Create many connections 
    - Application level DOS 
         - Exploiting vulns like 
              - Buffer Overflow 
              - SQL injection

## Tools For DOS 
- SolarWinds Security Event Manager (SEM) 
- ManageEngine Log360 
- HULK 
- Tor’s Hammer 
- Slowloris 
- LOIC 
- Xoic 
- DDOSIM 
- RUDY 1
- PyLoris


## Prevention ways 
- dos prevention 3rd company -- Cloudflare  
    - Limit or shut off broadcast forwarding where possible 
    - Set up firewalls
    - Eliminate and patch known vulnerabilities 
    - Monitor network inbound traffic