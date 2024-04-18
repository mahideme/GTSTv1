
# 📂Linux File Hierarchy

- file system is a directory structure that the OS uses.
- Linux/UNIX have a special file system than windows.

## SYSTEM FILES

- are files used by the  system software(OS).
   - **Windows** : system file appears under the ==local disk C:==
   - **Linux** : system files appear under the ==root directory(/)==.  / --- ye linux directory system mikemetbet

- **tilda = /home/username** --home directory



### 📂File structure 
1) / ( root ) 
     - Every single file and directory starts from the root directory 
     - The only root user has the right to write under this directory 
     - /root is the root user’s home directory, which is not the same as /

2) bin - Binary executables 
     - Essential command binaries that need to be available in single-user mode; for all users
         i) e.g) cat, ls, cp,pwd

3) /boot - Boot loader files 
      - Kernel initrd, vmlinux, grub files are located under /boot 
	       eg : initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic


4) /dev - Essential Device files ○
    - These include terminal devices, usb, or any device attached to the system. 
           Eg: /dev/tty1, /dev/usbmon0


5) /etc - et cetera 
     - Contains configuration files required by all programs. 
     - This also contains startup and shutdown shell scripts used to start/stop individual programs.          Eg: /etc/esolv.conf, /etc/logrotate.conf.


6) /home - Home directory 
      - Home directories for all users to store their personal files. 
           eg: /home/nathan, /home/rexder



7) /lib - Libraries essential for the binaries in /bin & /sbin 
    - Library filenames are either ld* or lib*.so.*
         Eg: ld-2.11.1.so, libncurses.so.5.7


8) /media - Mount points for removable media such as CD-ROMs 
      - Temporary mount directory for removable devices. 
            Eg: /media/cdrom for CD-ROM; /media/floppy for floppy drives; /media/cd recorder for CD writer


9) /mnt - Temporarily mounted file 
     - Temporary mount directory where sysadmins can mount filesystems.


10) /opt - Optional application software packages 
    - Contains add-on applications from individual vendors. 
    - Add-on applications should be installed under either /opt/ or /opt/ sub-directory


11) /sbin - Essential system binaries 
     - Just like /bin, /sbin also contains binary executables. 
     - The linux commands located under this directory are used typically by system administrator, for system maintenance purpose.




12) /tmp - Temporary Files 
     - Directory that contains temporary files created by system and users. 
     - Files under this directory are deleted when system is rebooted.



13) /usr - User Utilities 
     - Contains binaries, libraries, documentation, and source-code for second level programs. 
     - /usr/bin contains binary files for user programs. If you can’t find a user binary under /bin, look under /usr/bin. For example: at, awk, cc, less, scp 
     - /usr/sbin contains binary files for system administrators. If you can’t find a system binary under /sbin, look under /usr/sbin. 
	      eg: atd, cron, sshd, useradd, userdel, /usr/lib contains libraries for /usr/bin and /usr/sbin , /usr/src holds the Linux kernel sources, header-files and documentation.




# ⌨Text Editors 

- Programs That used for text processing. 
- Linux command line text editors 
     - VIM 
     - Nano 
     - Emacs 
     - Neovim 
     - …. 
- Linux Graphical Text editors 
     - Sublime 
     - Vscode 
     - Gedit 
     - Pluma 
     - …






# Linux user management 


whoami = username
hostname = machine name

creating user(user creating)
commands .. using sudo
1. useradd- less powerfull. 
         - eg: ==useradd *username*==
         - terminal type - sh
         - doesn't require password for the created user. 
         - they don't appear in the home directory (/home)
         - to add them on the home directory(/home)
             - command
                  - ==sudo mkhomedir_helper username==
        - to their terminal from sh
            - command   "-h"--  to ask for option
                  -  ==sudo usermod  username -s /bin/bash==
        - to give them password
             -  ==sudo passwd username==
         - to delete password of the user
             - ==sudo passwd -d username==
        - to delete completely simply uses ==sudo userdel username==
2. adduser - more powerfull. 
          - eg: ==adduser *username*==
          - terminal type - bash
          - it require password for the created user.
          - they appear in the home directory.
          - to delete password of the user
             - ==sudo passwd -d username==
          - to give them password
            -  ==sudo passwd username==
         - to delete the user permanently from all directory we use ==sudo userdel -r username== or ==sudo deluser --remove-home username==
          - it does remove user in ==sudo userdel username== but not earse its name from directory so use the above
to check if we create a user 
    - ==cat /etc/passwd==
    
sudo gives power --- only root have this power
     - to access root -> command
         - ==su -==
            or if we don't have root password
          - ==sudo su -==

for entering into other users
  -- commands
       -- ==su - other_username==
            or if password is unknown
       -- sudo su - ==other_username==

  - after we enter by user account, if we try to add another user  in that user account , we will denied because that user (the user account we entered) are not on the sudoers file.
  - so how can that user be  in the sudoers file like us?? he can't by itself so we(sudoers) can give him super power.
         -  to give him power 
            - 1st out from that user - : ==logout /exit/ctrl d== 
            - 2nd on the  home directory(/home) - :  ==sudo visudo==  -> on the "user privilege specification" , fill the form by username that we want to give.  eg : ==username  ALL = ALL== . then ctrl x or ctrl c -> to out.
        - then check if the user have the power like us
             - enter into that user -> ==sudo su - username==  - (actually if we can use sudo, it means we give him power like us but check for sure)
             - then check it if we add user -> ==sudo useradd another_username==
             - to see the created -> ==cat /etc/passwd==


to see password on linux - but it is encrypted 
    -> ==sudo cat /etc/shadow==
###### to delete users from that we created
>to remove users but not from the directory( username)
    -> ==sudo userdel username==  -- delete the user account but will not remove the user's home directory or any files associated with the user.
    -> ==sudo deluser username==  -- remove the user account and its primary group, but it will not remove the user's home directory or any files associated with the user.
> to remove permanently from the directories but **if we did give root access for the user it won't be out by this command so we have to delete it from sudoers file so go to ==sudo visudo==  then delete it.
     -> ==sudo userdel -r username== -- will delete the user's home directory and all files and directories within it. permanently removes the user's data.
     ->==sudo deluser --romove-home username== --Adding the `--remove-home` flag will delete the user's home directory and all files and directories within it. it permanently remove the users data
     
-> ==sudo rm -r /home/username== --permanently removes the file. from the home directory but not from data ( delete it from ls but not from cat /etc/passwd)

to group(collection of users that can share files) users that we created. in fact each user creates its own group
to know our groups ( foreach users)
     -> ==groups==
to create group
     -> ==sudo groupadd groupname==
to check for group
     -> ==cat /etc/group==
to give super power for that group 
     -> ==sudo visudo==  -> on the "allow members of group sudo ..." fill the form by the group name. eg: ==%group name  ALL = ALL== . then ctrl x, ctrl c.
      - therefore any users that are in this group will have this super power.
to add users to the group 
      ->==sudo usermod -aG groupname username==
to check if they joined the group
      -> ==cat /etc/group==
      -> ==groups==   - for each users.
then check if each users that are in the group, have a power as they are in the group that we already give super power.  ( if they can use sudo they have power)
- we can check for each user 
       ->==sudo su - username==
       ->==sudo useradd username==
therefore only users that are on the sudoer file have supper power.

to delete group 
    ->==sudo groupdel groupname==
to remove user form the group 
    -> ==sudo gpasswd -d username groupname==
    -> ==sudo nano /etc/group== -- using manual group file editing. -- Locate the line corresponding to the group from which you want to remove the user. -- Remove the username from the line, ensuring that the usernames are separated by commas. -- Save the changes and exit the text editor
