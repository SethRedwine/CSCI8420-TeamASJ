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

To mitigate elevation of privileges attacks, the UI is never given more privilege than the application. UI does not have direct access to memory. Any data passed between the UI and the application is authenticated as valid. 

### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/5)
