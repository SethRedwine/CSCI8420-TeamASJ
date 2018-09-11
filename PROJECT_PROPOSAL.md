# Project Proposal
## TeamASJY

### Project Motivation
---
Our first criteria was to select a project in common languages we all know or am able to pick up quickly. A common, well-established language will also have the security tool support to complete the project. Python meets both of these criteria.

Once we decided on Python, we began to look at projects on GitHub. Mailpile stood out as it seemed to inherently have a lot of interesting security features. On top of the typical security requirements required with email (i.e. user authentication, [FILL OUT]), Mailpile does some neat stuff with encryption and storing email locally on a user’s computer.

### Mailpile
---

**Description**

[Mailpile](https://www.mailpile.is/) is an email client built with a focus on security, making it easy for users to send and receive signed or PGP encrypted email.

The client is built mainly on Python, Javascript, and HTML and offered for macOS, Linux, and Windows. Though, the Linux distribution is the only offering not being reworked at the moment.

The project has three main contributors:

* [Bjarni R. Einarsson](http://bre.klaki.net/)
* [Smári McCarthy](https://smarimccarthy.is)
* [Brennan Novak](https://brennannovak.com)

But the project has received contributions from more than 140 contributors to date. The project has had 26 commits just in the last month and has incorporated over 550 pull requests over the life of the project, so it seems to be fairly active. Contributors can find a lot of good documentation on the project, from [design documents](https://github.com/mailpile/Mailpile/wiki/Design-documents) to a list of [keyboard shortcuts](https://github.com/mailpile/Mailpile/wiki/Keyboard-shortcuts), on the [wiki](https://github.com/mailpile/Mailpile/wiki).

**Links**

[Website](https://www.mailpile.is/)
[Repository](https://github.com/mailpile/Mailpile)
[Wiki](https://github.com/mailpile/Mailpile/wiki)


### Security Requirements
---
Users of Mailpile are very interested in security. As this is an email client, so it can be used at home or work for users. The most prominent feature is the encryption of email to a users local computer. Mailpile has no email servers of its own. Instead, it uses existing email addresses. Mailpile goes to the email servers to download the messages, then deletes the email the remote copy on the server while encrypting and storing the messages locally. Encryption keys are never sent anywhere. Deleting mail from the server isn’t perfect as it is unpredictable when a server will truly purge itself ot deleted data. But for common attackers that have gained access to an email account, they won’t find much since the messages have been deleted.

### Security Features
---
* Encryption - Mailpile advertises itself as not being an email service, but an email client. The developers state that Mailpile provides a strong encryption scheme.

* User Database Security - Mailpile does not have any type of user database. There is no server or any type of infrastructure that contains user information. The software does not track any information about the users of it.

* Secure Attachments - Email attachments are not stored through Mailpile directly. They are stored wherever the email message is stored on the users computer. This prevents malicious users from being able to access email attachments that are sent through Mailpile.

* Private Key Security - Mailpile does not store the users private keys on any type of mail server. Because Mailpile does not provide mail servers, it does not store any private keys. This allows users to have complete control over their private keys.

### Security History
---

[Security Roadmap](https://github.com/mailpile/Mailpile/wiki/Security-roadmap)
[Documented Issues](https://github.com/mailpile/Mailpile/issues?utf8=✓&q=label%3A%22Privacy+%2F+Security%22+)


### Licensing and Contributions
---

The Mailpile client is licensed under the GNU Affero General Public License (AGPLv3), which can be read about [here](http://www.gnu.org/licenses/agpl-3.0.html). This is a copyleft license that requires people to disclose any modifications made to the source code under this license but not any other part of their own code.

To contribute to Mailpile, the process seems fairly straightforward. One can find the Mailpile team’s guidelines [here](https://github.com/mailpile/Mailpile/blob/master/CONTRIBUTING.md). After checking the [FAQ](https://github.com/mailpile/Mailpile/blob/master/DEV_FAQ.md) and ensuring that the problem is indeed an issue, one can open a new issue documenting the problem, if it hasn’t already been documented. Then, submit a pull request with a description clearly describing both the problem and its solution. All contributions to the project are made under the same AGPLv3 license, but there is a tag of the code that is dual-licensed under both the AGPLv3 and the Apache License 2.0 that can be forked and developed independently.


### Team Repository
---

[Github](https://github.com/SethRedwine/CSCI8420-TeamASJY/)
