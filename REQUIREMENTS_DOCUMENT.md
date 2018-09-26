# Requirements for Software Security Engineering
## TeamASJY

### Data Flows and Use Cases

There are several important data flows to and from the Mailpile email client, our system of interest. For the purpose of our analysis, we will focus in on a particular set of potential users for Mailpile, journalists and their sources. These users would like to send and recieve confidential emails from the client on their own personal computers, they would also like to store these emails locally, not remotely, and finally they would like to be able to delete files securely. Accomplishing these tasks requires data to flow between the client and the user, the client and local storage devices, and the client and the users' remote email servers. The uses cases for both the journalists and the sources can be seen in the diagram below.

![Use Case Diagram](https://i.imgur.com/wUkogeS.png)

### Security Requirements and Misues Cases

### Alignment of Security Requirements

### Security-Related Configuration Issues
One of Mailpile's main features is that it is not an email service, but an email client. It doesn't run it's own email servers. Mailpile is used in conjuction with other email servers in order to provide a more secure way to get your email. When downloading Mailpile, you have to connect the client to your existing email accounts such as Gmail or Yahoo. Since users have to login to an external service using Mailpile, this connection and any credentials used to sign in would have to be encrypted to prevent unauthorized access. Mailpile provides built-in PGP encryption to handle this. According to the developers, at some point in the future, they want to offer an improved set of tools and integrations that make the email server component easier to integrate with. However, they have to make sure they do this correctly so they do not compromise security or ethics in the process. The developers also state that you may want to set up your own mail server using other open source projects such as Mail In A Box or iRedMail. 

Another security-related configuration issue is that Mailpile currently does not have any type of configuration file format. As of now, most of the initial configuration data is set so that is not required to be inputted. The developers want to have a safe way to import and export configuration data without leaking passwords or any other type of data. Mailpile is currently a very safe way to get your email and the developers are actively trying to implement more security features in order to make Mailpile safer to configure with external email services.

### Project Task Board
[Github Project Page](https://github.com/SethRedwine/CSCI8420-TeamASJY/projects/2)
