# Cryptography? 

- Cryptography is the **science of secret, or hidden writing** 
- **Crypto => Hidden/Secret** | **Graphy => Writing** 
- Used to **secure your data/text**.
- It has two main Components:
      a. **Encryption** 
        - Practice of **hiding messages** so that they **can not be read by anyone other than the intended recipient**
      b. **Authentication & Integrity** 
        -  **Ensuring** that users of data/resources are the persons they claim to be and that **a message has not been altered**


### Encryption Cipher 
encryption--- plain text to cipher(encrypted) text. opposite to decryption
- ==Cipher== is a **method for encrypting messages** 
- Encryption algorithms are standardized & published 
- The ==key== which is an **input to the algorithm** is **secret** 
- ==Key==: is a **string of numbers or characters** 

#### Symmetric Algorithms 
- Algorithms in which **the key for encryption and decryption are the ==same==**  
    Example: **Caesar Cipher** 
-  Types: 
     - **Block Ciphers **
        - Encrypt data **one block at a time** (typically 64 bits, or 128 bits) 
        - **Used for a single message** 
     - **Stream Ciphers**
         - Encrypt data **one bit or one byte at a time** 
         - **Used if data is a constant stream of information**


##### Substitution Ciphers 
###### Caesar Cipher 
Caesar Cipher is a method in which **each letter in the alphabet is rotated by three letters** 
###### Using a key to shift alphabet 
Obtain a key for the algorithm and then shift the alphabets 
  -  For instance if the key is word we will shift all the letters by four and remove the letters w, o, r, & d from the encryption 
  - We have to ensure that the mapping is one-to-one 
  - no single letter in plain text can map to two different letters in cipher text 
  - no single letter in cipher text can map to two different letters in plain text
###### Website: rot13.com 
Replacing the letters by 1 shift we can get different rotations. To do this we can use this website. This encoding is called **rot encoding** 

#### Limitation  for symmetric algorithm 
- Any exposure to the secret key compromises confidentiality of ciphertext 
- A key needs to be delivered to the recipient of the coded message for it to be deciphered 
    - Some intruders can get the key and BOOM! No secret anymore. 
    
Exercise 1 
1. Change “Pass1233” text to caesar Cipher 
2. What is the starting alphabet to produce “Rexler” text by shifting 
3. What is the encoding method of “Rexler” a. Answer: Rot__ 
4. Change “Hello There” to cipher with a key to alphabet shift of “HACK”



#### Asymmetric Encryption 
- Uses **a pair of keys** for encryption 
    - **Public key** for encryption 
    - **Private key** for decryption 
- **Messages encoded using public key can only be decoded by the private key** 
    - **Secret transmission of key** for decryption is **not required** 
          - **Public key can be exposed** so, if i need to send you a message i just ask you for your public key and i will encrypt the message with your public key. When you get the ciphertext you can decrypt it with your private key. 
    - Every entity can generate a key pair(private & public) and release its public key

##### Types of asymmetric enc. 
- Two most popular algorithms are RSA & El Gamal , AES, DSA
- RSA 
    - Developed by Ron Rivest, Adi Shamir, Len Adelman 
    - Both public and private key are interchangeable 
    - Variable Key Size (512, 1024, or 2048 bits) 
    - Most popular public key algorithm 
    - It have a maths formulas for generating the keys. 
- El Gamal 
    - Developed by Taher ElGamal 
    - Variable key size (512 or 1024 bits) 
    - Less common than RS
###### Applications 
One of example program that use asymmetric encryption is ==SSH==. When you Create/Config SSH on your computer it ==give u 2 keys,== 1 public and 1 private, so when connection is established each hosts exchange their public key and store it in (known_hosts), then anytime they send data they will encrypt them with the public, and the host will decrypt it with its private key. So if your Private Key got leaked💀


### 3 Terms of Cryptography 
1) **Encoding/ decoding** 
     - This is a method of **creating Cipher text with out using any key** 
     - This can be done by doing math on the given input/substitution    
         - Examples: base64,base32,rot…
2) **Encrypting/Decrypting** 
    - This is method of **creating Cipher text with keys**. 
    - To decrypts this kind u need to have the private key 
         - Example: DES,AES,RSA
the above are two way, reversible, (decryptable or decoded)
3) **Hashing** 
one way and irreversible, undecryptable, but cracked or **matched**
    - This is a method of creating Cipher text with respect to a created hash 
    - **To reverse the hash, you just search for some match, you don't decrypt/decode it**. 
    - **Salt:** is a random string used for data modification for password protection, This can be adding some text as prefix/suffix 
        - Example: MD5,sha254,...



#### Kinds of encodings/encryptions 
- Base2 01100010 01110010 01100101 01100001 01101011 01101001 01110100 == breakit
- Base8 142 162 145 141 153 151 164 
- Base16 62 72 65 61 6b 69 74 
- Base32 MJZGKYLLNF2A==== 
- Base58 4jP4KDubX1 
- Base62 22udqyscMu 
- Base64 YnJlYWtpdA== 
- Base85 @WH$gCM@k 
- Base91 %zmfv;:YH 
- URL encode: hello%20there%20%3F 
- Md5: 5d41402abc4b2a76b9719d911017c592 
- Sha1: aaf4c61ddcc5e8a2dabede0f3b482cd9aea9434d 
- Rot : Uryyb, Frphevgl Grfgref

### tools  
- There are lots of encodings/encryption 
- To identify this we will need some tools/sites
- Tools:   
    - ==Cyber chef== -- web
    - ==Tunnelsup== -- web
    - hashid --hash--  on linux

#### decoding/decrypting 
There are so many way to reverse some hashes/ciphers. 
- Hashes 
       - ==Crackstation.net==(non-salted)  
       - Own cracking(google the name) 
 - Encodings 
      - ==CyberChef==


**identifying unknown hashes**
some hashes are not normal hashes they are generated by some Platform/Software. So to Crack this hash. - Identify the Software which the hash Generated with.
- Ex: The Hash can be generated by some Software called Openfire 
- Then Try to Search Some Cracking Scripts made for this has


## Wordlists 
- Wordlists are a normal text file that contains Different Words that can be used to match hashes, or for checking some parameters repeatedly using some loops

#### Custom Wordlists 
- We can Create our own Wordlists, We can Create text file and add our highly usable words or we can use tools like 
    - Cewl
    - Cupp



# Python for cryptography 
- We can use programming to do tools that can do our own encryption and encoding hash type 
- There are so many methods, even you can do the encoding/decodeing for the base64… 
- You just need to understand the maths. 
- simple XOR’ing example 


- Unicode is a character encoding standard that assigns a unique numerical value, called a code point, to each character or symbol. The Unicode decimal representation refers to expressing these code points as decimal numbers.
- The Unicode decimal representation simply converts these hexadecimal code points to their decimal equivalent.
     - The Unicode code point for the uppercase letter "A" is U+0041 in hexadecimal.
     - The decimal equivalent of U+0041 is 65.
encrypt
- change the message and the key into unicode decimal and then xor it with the key
- after xor change the output to hex data
decrypt
- hex data to unicode for the message --bytes.from hex().decode()
- unicode to message xor with key -- ord
- converts the unicode text into characters -- chr


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



## Obfuscation 
-  In software development, obfuscation is the act of creating source or machine code that is difficult for humans or computers to understand. ● As we know High level programming lang. are easy to understand, so if hackers got your code he can read it, but to make it more difficult we use this technique ● This was the codeni