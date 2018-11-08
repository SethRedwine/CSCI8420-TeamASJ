# Design Document
## TeamASJY

### Threat Models

### Mailpile Security Analysis Summary

Mailpile uses a variety of strategies to mitigate security concerns. In its communication with email servers, it uses PGP, SSL, and TLS encryption. These protocols can be found mainly in auth.py and conn_brokers.py files of code. When the data is downloaded from the server, it is saved to the hard drive using the WERVD protocol. 

### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/5)
