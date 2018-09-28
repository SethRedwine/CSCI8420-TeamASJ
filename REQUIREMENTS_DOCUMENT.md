# Requirements for Software Security Engineering
## TeamASJY


### Data Flows and Use Cases

There are several important data flows to and from the Mailpile email client, our system of interest. For the purpose of our analysis, we will focus in on a particular set of potential users for Mailpile, journalists and their sources. These users would like to send and receive confidential emails from the client on their own personal computers, they would also like to store these emails locally, not remotely, and finally they would like to be able to delete files securely. Accomplishing these tasks requires data to flow between the client and the user, the client and local storage devices, and the client and the users' remote email servers. The uses cases for both the journalists and the sources can be seen in the diagram below.

![Use Case Diagram](https://i.imgur.com/oe9yyB9.png)

Figure 1: Use Case Diagram



### Security Requirements and Misuse Cases

For our analysis of security requirements for Mailpile, it was useful to split our use cases into two separate views - those use cases that involved communications with systems external to the user's local machine and those that didn't. For the use cases that required communication with email servers over a network, both sending and receiving emails, the email client is vulnerable to the same types of attacks that any networked application is. The main concern we identified was eavesdropping on network traffic, because the client is directly accessing the emails on the server. In our journalist example, this type of malicious activity could allow a bad actor to identify a journalist's source and what they are communicating to the journalist; this bad actor could be an entity that a journalist is covering or a rival journalist trying to cover the same story. An easy way to prevent this type of attack would be to encrypt traffic between the client and the server. Another concern was that an attacker might gain access to the user's email directly on the email server and possibly manipulate them or delete them entirely, which would defeat the purpose of using Mailpile. To mitigate the ability of an attacker to access emails directly on the server, the client could delete the emails from the server once they have been downloaded to the user's local machine.

![External Misuse Cases]()

Figure 2: External Misuse Cases

The security requirements for use cases pertaining just to the local machine also follow a familiar pattern. Here, a disgruntled article subject may wish to identify a source or get rid of information about them or an editor, being pressed to prove an article is true may wish to identify a source used by the journalist. These misuse cases would require the bad actors to gain access to either the mail client itself or to the contents it has stored on the local disk. Assuming that the bad actor has already gained access to the journalist’s device, for example if the journalist works from a shared machine, there are a few ways that Mailpile could mitigate against attacks. The first way to protect against misuse on the local machine would be to require a login to use the email client, though, if an editor wanted to gain access to the email it’s not hard to imagine that they could just wait until the journalist has left their device unattended with the client open. To further mitigate this possibility a timeout on the login could be used. If the misuser happened upon the client and it was already locked they may try to brute force the password, which could be remedied by a graduated password entry delay after so many failed attempts - similar to a phone's lockout.

![Login Misuse Case](https://i.imgur.com/w2x0d0w.png)

Figure 3: Login Misuse Case

Protecting the emails locally also requires that the files where the emails are saved are secure. Again this could be alleviated with encryption, with the contents only being decrypted when the client is opened and the user has logged in.

![Local Misuse Cases]()

Figure 3: Local Misuse Cases


### Alignment of Security Requirements

Mailpile advertises itself as being an extremely secure way to view your email. Because of this, there are numerous security requirements that must be enforced and all of these must align together with the main goal of the project. The misuse case diagrams shown above highlight what security requirements are needed to keep Mailpile users safe. One of the larger threats to email security is having emails stored online in a mail server. Since Mailpile deletes emails off the remote server after it downloads them, it prevents this problem from happening. Along with this, all network communication within Mailpile is encrypted with OpenPGP. This prevents bad users from monitoring network traffic or being able to capture email contents.

Other security requirements that were identified include preventing malicious users from getting access to emails within somebody else's Mailpile client. These problems are addressed as Mailpile requires credentials to login to the client. These credentials are securely stored locally as Mailpile does not keep a database of users. Other features include a login timeout in case malicious users try to simply wait for a user to leave their client open.

One weakness that was identified with the project is that Mailpile is currently interoperating with existing security standards. This can be considered a weakness because the current standards may be lacking in some ways regarding security requirements. As mentioned earlier Mailpile uses OpenPGP encryption. This standard does not encrypt email message headers, so the message subject, sender, and recipients remain unencrypted. The developers are actively trying to improve these features and incorporate better security measures so that the security requirements are better aligned with the features that the users of Mailpile need.

Another weakness that is outside of Mailpile's control is the data retainment policy of the email provider. Even though it deletes the email from the server, it could still be kept in remote data backups. There is no way to force the email provider to get rid of a backup. A hacker could theoretically find the data that way, but it is unlikely that would happen. Most hackers will likely stop once they see the account is empty. 

### Security-Related Configuration Issues

One of Mailpile's main features is that it is not an email service, but an email client. It doesn't run it's own email servers. Mailpile is used in conjunction with other email servers in order to provide a more secure way to get your email. When downloading Mailpile, you have to connect the client to your existing email accounts such as Gmail or Yahoo. Since users have to login to an external service using Mailpile, this connection and any credentials used to sign in would have to be encrypted to prevent unauthorized access. Mailpile provides built-in PGP encryption to handle this. According to the developers, at some point in the future, they want to offer an improved set of tools and integrations that make the email server component easier to integrate with. However, they have to make sure they do this correctly so they do not compromise security or ethics in the process. The developers also state that you may want to set up your own mail server using other open source projects such as Mail In A Box or iRedMail.

Another security-related configuration issue is that Mailpile currently does not have any type of configuration file format. As of now, most of the initial configuration data is set so that is not required to be inputted. The developers want to have a safe way to import and export configuration data without leaking passwords or any other type of data. Mailpile is currently a very safe way to get your email and the developers are actively trying to implement more security features in order to make Mailpile safer to configure with external email services.



### Project Task Board
[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/2)


