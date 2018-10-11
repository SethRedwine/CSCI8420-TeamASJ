# Assurance Cases Document

## TeamASJY

### Assurance Claims

#### 1. The client prevents all unauthorized access.

![Assurance Case 1](https://i.imgur.com/exehQUp.png)

**Evidence:**
* Evidence 1: [FAQ](https://www.mailpile.is/faq/#enc-5)
* Evidence 2: [auth.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/auth.py) 
* Evidence 3: We could not find any evidence in the source code that this feature exists. Once implemented, then we                   would point this evidence to where the login attempt counter would be located.
* Evidence 4: [security.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/security.py)

#### 2. The client prevents unauthorized access to saved emails.

![Assurance Case 2](https://i.imgur.com/R3pYW9t.png)

**Evidence:**

* Evidence 1: [WERVD Storage](https://github.com/mailpile/Mailpile/wiki/WERVD-Storage)
* Evidence 2: C3 is an important subclaim to prove C1, but we could find no evidence that steps had been taken to support this claim. This leads us to believe that this is a potential flaw in the security of Mailpile. Easy ways to prove this claim might include attempting to hide the data store or simply changing the file permissions for the files.
* Evidence 3: [mailpile-test.py](https://github.com/mailpile/Mailpile/blob/master/scripts/mailpile-test.py)
* Evidence 4: [auth.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/auth.py)


#### 3. The client's communication with external servers is secure.

![Assurance Case 3](https://i.imgur.com/6HGqliT.png)

**Evidence:**
* Evidence 1: [conn_brokers.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/conn_brokers.py)
* Evidence 2: The evidence would have to be collected using something like WireShark to monitor network traffic while Mailpile is running.
* Evidence 3: [security.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/security.py)

#### 4. The client protects the identities of the sending and receiving parties.

**Evidence:**
![Assurance Case 4](https://i.imgur.com/e3L0jW5.jpg)
*  Evidence 1: The communication text will be changed all the time. Therefore, the PGP encryption will also encrypt messages differently and changing all the time.
*  Evidence 2:[PGP description part](https://info.townsendsecurity.com/bid/66064/aes-vs-pgp-what-is-the-difference)
*  Evidence 3:[Is Mailpile webmail like Gmail, Yahoo, Hotmail?](https://www.mailpile.is/faq/#wha-3)
*  Evidence 4:[Security quality](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)

#### 5. The client provides secure remote access to the contents.

### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/4)
