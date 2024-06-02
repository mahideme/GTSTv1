 

# Further on user management

to change user id 
sudo usermod -u 1239 hana


#### installing software on Linux (hacking tools)
android is linux kernel based OS
package manager - is like google play ...  it seizes different applications or packages discription details and put like  repository then download it from that.
A package manager on Linux is a software tool that helps users install, update, and manage software packages on their Linux distribution. It simplifies the process of installing and maintaining software by handling dependencies, version management, and package installation from official repositories or other trusted sources.

command 
 --> ==man *command*== --to ask for any commands
##### two ways
1. debian package manager(dpkg)
    - need the application software download link
        -    to install
              - ==sudo dpkg -i link==
        - not good because when there is dependency it doesn't work
2. apt
      - ==sudo apt search yourprogram== -- if we don't know full name
      - it is like google play. apt download the softwares and there dependenceis from repositories (online database). this is updated frequently but the computer was updated when it was downloaded so the computer must be update for new version. to update (to connect apt with the updated repository) ==sudo apt update== . 
      - then download the software
            - ==sudo apt search yourprogram== 
            - ==sudo apt show yourprogram==  to know about yourprogram 
            - ==sudo apt install correct_name_ofyourprogram==
        - it also download dependencies
    - to uninstall 
             - ==sudo apt remove yourprogram== - only that program not for dependency
             - so to delete additional package ==sudo apt autoremove== 

      -  where are these repository located
           - more programs work for ubuntu so to access them on kali linux we have to edit the repository -
                -- ==sudo apt edit-sources== 
                 - continue with default (1 nano)
                 - click the ctrl on necessary link - it goes to the repository so apt copies the files (links) from this. if we want for ubuntu  -- search for **ubuntu repository sources** then find the link -- copy and paste to the terminal then ctrl x. then update it  ==sudo atp update ==

#### to download hacking tools

from the git hub

==git clone link==



# Linux Run 

 ### Linux file permission

- on command ==ls -l==, there are many things 
-  Every file on linux have their own 
      -  Owner 
      - Permissions 
- There is 5 main parts on the listing 
       - Permission                  
       - Owners 
       - Date 
       - Size 
       - filename
                  ![[Pasted image 20240419182824.png]]

- Ownership 
     - is the owner of the file 
     - This have 2 kinds 
          - User   - Group 
     - To **change the owner of file** you can use the command 
            ==chown user:group filename==  -- to change **both**
            ==chown username filename==  -- to change **only the user**
            ==chown :newgroup filename== -- to change **only the group**
            ![[Pasted image 20240420132528.png]]


Permission 
- There are 3 types of permissions 
     - Read ( r ) 
     - Write ( w ) 
     - Execute ( x ) 
- The folders and files are differ with the ‘d’ and ‘-’ on the beginning of the permission.
- There still the permission have three parts. 
       - user -group-other 
- User ( u ) => power of user defined on the the ownership 
- Group (g )=> power of group defined on the the ownership 
- Other ( o ) => power of other users. 
- All ( a ) => power of all which can be found in the 3 above owners 
- Command to **change permission** of file 
      ==chmod +/- x/w/r  filename==
  ![[Pasted image 20240419185230.png]]
  - CHMOD command 
     - This command helps to change file permission. 
     - Those file permissions are read, write & execute. 
     - Each of the permission have a number representations. 
          - Read -> **4 - r** 
          - Write -> **2 - w** 
          - Execute -> **1 - x** 
    -  ==chmod "parameters" filename==
- The parameter can be in numbers and symbols 
   A) Parameters in symbol 
      - chmod a+x filename -> adding execute permission for all ( chmod +x filename) 
      - chmod **u+x** filename -> adding execute permission for user **it can be w or r**
      - chmod **g+x** filename -> adding execute permission for group 
      - chmod **o+x** filename -> adding execute permission for other 
      - chmod **-x** filename -> removing execute permission for all 
      - chmod **a+rwx , u-rw , g-x , o-xw** filename -> gives rwx for all and removes something from all 
    B) Parameters in Number 
     chmod **621** filename -> **u+rw, g+w, o+x** 6 for user, 2 for group, 1 for other ( 6 = 4+2 ), 6 
      chmod **777** filename ->**a+rwx** 7 for users, 7 for group , 7 for others (7 =4+2+1), 7 


1. Create file called “Perm.txt” and give the following permission to it  --w-r----x

          ![[Pasted image 20240420140801.png]]

2. What is the equivalent of 631 permission in symbolic?
      -  -rw--wx--x  / drw--wx--x

3. What is the equivalent of 200 permission in symbolic? 
     - --w-------  / d-w-------

4. What is the numeric equivalent of -rwxrw-rw-
     - 766
5. Create a user called gtst & test with password 123456 
6. Change the file user owner of Perm.txt to gtst and the group owner to root
     ==sudo chown gtst:root perm.txt==
7. Change the user password of gtst to “pass123” 
8. Change the user id of ‘gtst’ to 1923 
9. Delete the user ‘test
      ![[Pasted image 20240420143948.png]]
      ![[Pasted image 20240420144017.png]]
      ![[Pasted image 20240420144036.png]]


### Special File Permissions
- There are another 3 special permissions, you may encounter on your pentest Journey.
- They are 
     - SUID bits(s) - set user ID bit - add 4 infront of our numeric value -> 4000 
     - SGID bits(S) - set group ID bit - add 2 infront of our numeric value -> 2777 
     - Sticky bits(t) - set other ID bit - add 1 in front of our numeric value -> 1602 - 
- They are permissions like the execute(x), but they will set the execute permission to the user who settled them.
- Example: if mr.A add suid bit to a program that program will be executed with permission of mr.A 
     - Meaning if admin add suid bit on some program. Then any user if they got that program they can run it as root with any sudo password.



Package installation on linux 
- ON linux to install softwares you use package managers. ○ Ex: apt,pacman,pkg,...  
- We will use debian package manager. 
- On debian the package manager i called ‘APT’ also there is called ‘dpkg’ 
- Package managers are a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions




 # from 4:00 to 12:00-- gtst linux finishing 
 comparch  12-1: 30-- chapter two 
 chapter 1 5- 6
 chapter 1 and 2 -- 11: 30 - 1: 30