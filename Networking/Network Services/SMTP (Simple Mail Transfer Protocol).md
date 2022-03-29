- SMTP or Simple Mail Transfer Protocol is used simply to handle the sending of emails. It's sibling POP/IMAP is used for retrieving incoming mail.
- The SMTP server performs three basic functions.
	- It verifies who is sending emails throught the SMTP server.
	- It sends the outgoing mail.
	- If the outgoing mail can't be delivered it sends the message back to the sender.
- Typically you will only encounter SMTP when configuring a third-party email client such as Thunderbird.
- SMTP combined with POP/IMAP works as follows
	- The mail user agent, which is either your email client or an external program connects to the SMTP server of your domain, e.g. smtp.google.com. This initiates the SMTP handshake over the designated port (typically port 25)
	- The mail is now sent first as the sender and recipient's email address, the body of the email, and any attachments to the server.
	- The SMTP server then checks whether the domain name of the recipient and the sender is the same.
	- The SMTP server then will make a connection to the recipients SMTP server, if it can't be accessed the email is put into a queue.
	- The recipients SMTP server will verify the incoming email by checking the domain and user name have been recognised. 
	- The email will then show up in the recipient's inbox.
	- 

<img src="https://github.com/TheRealPoloMints/Blog/blob/master/Security%20Challenge%20Walkthroughs/Networks%202/untitled.png?raw=true">
