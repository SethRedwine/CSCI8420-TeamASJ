# Assurance Cases Document

## TeamASJY

### Assurance Claims

#### Claim 1: The client prevents all unauthorized access.

![Assurance Case 1](https://i.imgur.com/WJJ2B5P.png)
*Assurance Case 1*

**Evidence:**
* Evidence 1: [FAQ](https://www.mailpile.is/faq/#enc-5)
* Evidence 2: [auth.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/auth.py) 
* Evidence 3: We could not find any evidence in the source code that this feature exists or that steps had been taken to support this claim. This could be considered a potential security flaw of Mailpile. If this feature was implemented in the future, then we would point this evidence to where the login attempt counter would be located in the source code.
* Evidence 4: [security.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/security.py)


#### Claim 2: The client prevents unauthorized access to saved emails.

![Assurance Case 2](https://i.imgur.com/2JnnbyI.png)
*Assurance Case 2*

**Evidence:**

* Evidence 1: [WERVD Storage](https://github.com/mailpile/Mailpile/wiki/WERVD-Storage)
* Evidence 2: C3 is an important subclaim to prove C1, but we could find no evidence that steps had been taken to support this claim. This leads us to believe that this is another potential flaw in the security of Mailpile. Easy ways to prove this claim might include attempting to hide the data store or simply changing the file permissions for the files.
* Evidence 3: [mailpile-test.py](https://github.com/mailpile/Mailpile/blob/master/scripts/mailpile-test.py)
* Evidence 4: Assurance Case 1


#### Claim 3: Mailpile prevents eavesdropping between the client and the email server.

![Assurance Case 3](https://i.imgur.com/Z7147H5.png)
*Assurance Case 3*

**Evidence:**
* Evidence 1: [conn_brokers.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/conn_brokers.py)
* Evidence 2: The evidence would have to be collected using something like WireShark to monitor network traffic while Mailpile is running.
* Evidence 3: [security.py](https://github.com/mailpile/Mailpile/blob/master/mailpile/security.py)


#### Claim 4: The client protects the identities of the sending and receiving parties.

![Assurance Case 4](https://i.imgur.com/BOLK0Rz.png)
*Assurance Case 4*

**Evidence:**
*  Evidence 1: This evidence would be collected by gathering different encrypted text files based on different email messages. This would show that the messages are all different from each other. Also, if the PGP encryption algorithm gets updated, this evidence would include change logs for that as well.
*  Evidence 2: [AES vs. PGP Article](https://info.townsendsecurity.com/bid/66064/aes-vs-pgp-what-is-the-difference)
*  Evidence 3: [FAQ](https://www.mailpile.is/faq/#wha-3)
*  Evidence 4: [PGP Description](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)


#### Claim 5: The client prevents unauthorized access through it's remote login. 

![Assurance Case 5]()
*Assurance Case 5*

**Evidence:**



### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/4)
