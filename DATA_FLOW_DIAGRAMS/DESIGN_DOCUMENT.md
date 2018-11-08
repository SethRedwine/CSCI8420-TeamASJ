# Design Document
## TeamASJY

### Threat Models

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


### Mailpile Security Analysis

#### Elevation of Privilege

#### Denial of Service

#### Spoofing

#### Tampering

#### Repudiation

#### Information Disclosure

When sending and receiving email, Mailpile uses PGP Standards for encryption. This is found in mailpile/auth.py file. To establish the keys to be used, Mailpile will (from ):
1.  Generate Autocrypt-compatible keys for all users when Mailpile is first installed.
  * mailpile/crypto/autocrypt_utils.py - This file is used for the general autocrypt functions. It parses the header and extracts the necessary keys.
2.  Help users make safe backups of their key material and passphrase.
  * mailpile/auth.py - Uses user sessions to authenticate against a passphrase.
3.  Sign mail by default, encrypt when the user requests it or there is a reasonable expectation that the recipient will be able to read it.
  *
4.  Distribute public keys as Autocrypt headers, or by attaching them to outgoing mail.
5.  Assess key validity using a "Trust upon first use/contact" (TOFU) strategy.


End-to-end communication with be protected with TLS.

### Project Task Board

[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/5)
