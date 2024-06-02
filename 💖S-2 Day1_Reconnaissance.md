
# Information Gathering/Foot-printing/Recon


- is **Collecting data** about some **network/host/system**. 
- Foot-printing => Footstep + printing(logging)-- memezgeb 
   -  it is a very important part of Ethical Hacking. Almost **85% of Hacking**.

## Why do we need recon? 
- Imagine, You are going to rob a bank… what do you do? 
    - Know How much polices are there in the bank 
    - Know the doors (way in and out ) 
    - Know if there is cctv 
    - Know which person is the CEO 
    - Know which time is Good for robbery 
- **To Get access on system 1st you have to know the system**. 
- **Knowing the system will lead you to know if the system is vulnerable.**

# Types of information gathering 

Based on **how we do the recon**

1) **Active** Foot-printing 
    - **Gather information directly by contacting that person.** 
         - Example: - When you go to the bank and ask for some information. 
                - Chatting with person on social media to know about them. 
     - Doing Active Foot-printing **without permission is ILLEGAL!!**


2) Passive Foot-printing 
    - **Gather information from another person,3rd party or by checking public sources.** 
            - Example: - To know the bank working time on the posted texts. 
                    - To know someone name by reading the username.


## 👀✍🏻What type of information do you gather? 
- We gather information for different things 🔎
     A. Host 
        -  Websites 
        - Computers 
        - Smart Phone 
     B. Network 
        - Home Network 
        - Companies network 
     C. Person/Organization
     D. Application
## 🏹📐How do we gather information? 
-  the techniques and methods we use can be little different. 

### A. Websites 
- 👀The **information** we gather about a websites are 
    - IP Addresses
    - Development frameworks 
        - Technologies used and versions 
    - Name 
    - DNS information (domain name)
    - Subdomains, Assets, Contents

- 🏹To **get IP address** of some website by **using Linux commands**
    -  Active recon 
         - ==ping== < website link >   (like **ping google.com**) webun host yaregubet ye **serverachewn ip** ysetenal
         - ==nslookup== < website link >  also give us ipv6 
         - ==host== < website link >  also gave ipv6
         **!! Don't add the https**
         **!! this is done by requesting the website for ip address** 
         **!! so, we are not secured. we are known by the website that we are gather info about them**
    - Passive recon 
         -  www.nslookup.io
         **!! this website will request and get the ip address of the website that we look for and finally give to us**
         **!! so, we are secured.**
     
 - 🏹To **get development frameworks** 
     - Use simple **browser extension** - are small software to extend the functionality of browsers
         - ==Wapplyzer== - used to find out the technologies, services, features running on a website.
                    - uncovers the technologies used on websites.
                    - It **detects** content management systems, ecommerce platforms, **web frameworks**, server software, analytics tools and many more.
         - ==Builtwith== 
     - **Terminal tool** - on Linux
         - ==whatweb==

- 🏹To **get the name** 
     - You can see the title of the website or texts inside the page also the URL.

- 🏹Details about **domains** 
     - For this you can use **whois terminal +website tool** 
         - sudo apt install whois 
         - whois 
         - dig


### B. Computers/Phone 
- 👀The information we gather about a Computers/Hosts are   
     -  IP Addresses 
      - OS information
      - Host-Name (computer name)
      - MAC address 
      - Open services or ports 
- Detail on “Scanning and Enumeration”


### C. Networks 
- 👀The information we gather about a Networks are 
     - IP Addresses 
     - Architecture 
     - Class and Type of Network 
     - Subnets / VHOSTs 
     - Hosts on that Network 
     - Strength and security of that Network 
- Detail on “Network Penetration testing”


### D. Personal Information
- 👀The information we gather about a Persons are 
     - Full Name 
     - Address 
         - Physical Address 
         - All Social Media Address 
         - Phone address 
     - What the person loves 
     - Job 
     - Friends 
     - Status 
     - skills 
     - ...
- 🏹use **passive technology** 
     - ==OSINT==

####          OSINT - Open Source Intelligence 
- Persons information can be gathered by active and passive. 
- Gathering and Analyzing Different Information **Based on Public resource Passively is called OSINT**.
- We can get lot of information for system, user, host,... through passive activity. 
- There are many **methods**, Lets See about Personal information. 

##### Getting Names by Phone number. 
- For this purpose you can use https://www.truecaller.com/ 
- You can get the phone number from social media like telegram, some posted promotion, from websites.
##### Getting social medias Addresses 
- If you have Full name of a person, Just use search engines(google, Bing, yahoo).
- Also you can use **tool called sherlock from github** -- on Linux terminal.

##### Getting Physical Addresses 
- Peoples share there living place **on social medias info page.** ( on fb )
- Else there are many methods: 
     - **Sending links** and when people access the link u can **get the IP** then you can just **geolocate the place.**( but not accurate in Ethiopia)
 #####  IP geolocation 
  -  If you got the private ip address of someone you can **insert it to** https://www.iplocation.net 
  - The method of getting the IP might be tricky. detail on Social Engineering note.

##### Knowing people's behavior and Obsession
- Peoples are being open on social medias, so we Security Testers have access about person behaviors' and likes.  
    - Example: - Instagram is the best place to get info about some user. 
             - Also by seeing telegram Profiles you can get more information about their religion status, mindset, ideology, family 
             - By checking their followings/friends you can get more common pictures and events, etc.…. 
**THIS IS #OSINT!!!**
Detail on Social engineering.


### E. Applications/Software 
- 👀The information we gather about a Applications are 
     - What they are made up of 
         - Which programming language used 
         - Which framework used 
     - Source codes 
     - Their logic and Function …


Exercise 1 
1. What is the IP Address of https://moe.gov.et/  -- ping moe.gov.et 
2. What is the IPv6 of https://google.com/  -- host google.com / nslookup 
3. What is The Full Name of This phone number owner +251911842577  -- https://www.truecaller.com/ -- Hayilu Beyene
4. What is the job of user called “Zelalem moges”?  using  google or using terminal - sherlock  --- assistance at aau
5. What is the Javascript framework of Youtube? -- use browser extention Wapplyzer or command "whatweb" ---  polymer


# Reverse image search 
part of OSINT
- is a technique of **searching with images**. 
- We all search with text but we can search with images too. This can give as more information
- Ex: think like user posted a picture with a background of some area, if the user didn't talk about the place we can just search the image and the search engines will give as some similar photos where they are taken in same place(not 100% accurate) 
- 🏹We can use: 
     - https://tineye.com/ 
     - https://www.labnol.org/reverse/ 
     - https://images.google.com/



# Google Dorking(Google Hacking)
- it's not hacking into Google servers! 
- Google hacking is about **using different Google operators to effectively optimize search results.** 
- It also involves **using Google to identify vulnerabilities in websites.** 
- Results are **highly customizable.** 
*- THIS IS THE MOST POWERFUL SKILL OF HACKER!*

## Basic operators 
- ==(+)==For **inclusion** of something common 
     - *Nathan Hailu +geeztech +ceo*   -> don't add space between the sign and the word 
- ==(-)== Terms you want to **exclude** 
     - *Antivirus -software*
     - *Georgia -America -state*
-  ==(“)==Search for an **exact term**
     - *"how to eat food"*
     - *“Nathan Hailu”
- ==( * )== **any word** (wild card) 
    -  If you include * **within a query**, it tells Google to try to **treat the star** as a **placeholder for any unknown term(s)** and **then find the best matches**. 
- ==( | )== Boolean ‘OR’
     - "Nathan Hailu" |  "Natan Hailu"



## Advanced Operators 
- These are **Syntaxes** **used by Google**. 
        - ==intitle== 
            - **Google returns results** with the word/phrase **found within the title of the page** 
                 - intitle:index.of 
                 - intitle:”Hackers Bible” 
        - ==inurl== 
             - Finds a **specific term** **within the URL** 
                 - inurl:view/index.shtml 
        - ==filetype== 
             - Searches for a **specific filetype** 
                 - “Hacking” filetype:pdf 
                 - filetype:txt 
        - ==Intext== 
             - Google returns links that contains Texts from that link. **on the body** 
                 - intext:”Hackers in Ethiopia”
 ## Mixing Operators
 - inurl:securethiscompany.com intitle:index.of
 - "mysql dump" inurl: filetype:sql intext:password
 - inurl:ftp "password" filetype:xls
 - intitle:admin intitle:login
- webcamXP - provider of webxam. some of them didn't ask for login username and password by default. 
      - intitle:"webcamXP" inurl:8080

#### GHD - Google hacking Database
- Link: https://www.exploit-db.com/google-hacking-database  --- google syntax for ethical hacking purpose
#### ‼WARNING
- If you do a lot of Dorking with same ip address, Google will block you for some hours, and shows you this. This is Because Google Want to Get rid of Bots/Scripts.

Exercise 1.
1. Hey Mr. Hacker give the the pdf file of the “systems engineer” from insa.gov.et site. a. Hint: some files are named in another language. -- ==inurl:insa.gov.et  filetype:pdf  "system engineer"==
2. What is the text file from insa web-site. --  ==inurl:insa.gov.et  filetype:txt
3. Give me screenshot of GHD result of That displays Nathan Hailu with geeztech only. -- ==intitle:"index of" "username"==  -- intitle:Nathan Hailu intext:geeztech 

    ![[Pasted image 20240519162222.png]]