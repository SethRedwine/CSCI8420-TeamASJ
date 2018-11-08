# Design Document
## TeamASJY

### Threat Models

### Mailpile Security Analysis

#### Internal Data Flows

![Internal Level 0 DFD](https://i.imgur.com/AV3WEji.png)

*Figure 1: Internal Level 0 DFD*

![Internal Level 1 DFD](https://i.imgur.com/WPKahb7.png)

*Figure 2: Internal Level 1 DFD*

[Analysis Report for Internal DFDs](http://htmlpreview.github.io/?https://github.com/SethRedwine/CSCI8420-TeamASJY/blob/master/DATA_FLOW_DIAGRAMS/InternalDataFlowReport.htm)

#### External Data Flows

![External Level 0 DFD](https://i.imgur.com/XmuXBcg.png)

*Figure 3: External Level 0 DFD*


![External Level 1 DFD](https://i.imgur.com/eD7mkt4.png)

*Figure 4: External Level 1 DFD*

[Analysis Report for External DFDs](http://htmlpreview.github.io/?https://github.com/SethRedwine/CSCI8420-TeamASJY/blob/master/DATA_FLOW_DIAGRAMS/ExternalDataFlowReport.htm)


### Security Summary

Mailpile uses a variety of strategies to mitigate security concerns. In its communication with email servers, it uses PGP, SSL, and TLS encryption. The connections are authenticated using usernames and passphrases. These protocols can be found mainly in auth.py and conn_brokers.py files of code. When the data is downloaded from the server, it is saved to the hard drive using a WERVD implementation. This is done using AES-256-CBC encryption with a per-file nonce.


From our observations, the internal communication between Mailpile and a machine's local storage is very secure. The communication between the Mailpile client and external mail servers is also very secure. Spoofing attacks are completely mitigated as Mailpile uses robust authentication mechanisms to validate users. OpenPGP encryption is used to secure passwords that have to be stored on the machine. This is done within the auth.py authentication program. Tampering attacks are not too much of a threat to the internal process of Mailpile as we are assuming a malware free system. There are input validation processes in place to validate any user input that is being sent to the internal virtual file system. There are some potential vulnerabilities regarding repudiation attacks. The internal processes of Mailpile do not have many logging mechanisms in place so it isn't able to cross-check any data with logged data. This could be a potential security issue if any malicious data makes it through the initial data validation process. Information Disclosure attacks are well protected against since Mailpile uses secure OpenPGP encryption to protect all of the internal keystores. Also, since we are assuming a malware free machine, data sniffing attacks will not be a problem. Denial of Service attacks within the internal process of Mailpile are extremely unlikely. Mailpile does have some protections in place to prevent this such as being able to end processes that are sending a very large number of requests over a short amount of time. It appears the developers of Mailpile are actively implementing more and more protections against Denial of Service attacks. Elevation of Privilege attacks are also well mitigated since Mailpile uses very secure user authentication. This type of attack is well known to the developers and they are actively enhancing Mailpile to protect against these attacks further. Overall, Mailpile seems very secure as it has numerous security features in place. The developers of Mailpile are also active in improving the security of the client as they are continually updating the software to better align with their security roadmap.

### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/5)
