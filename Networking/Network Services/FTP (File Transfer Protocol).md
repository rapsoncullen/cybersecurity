- FTP or File Transfer Protocol is... a system for transferring files over a network in plain english somewhat similar to [[Telnet]]  It works as follows
	- FTP operates over a 
		### Client-Server Protocol
		- The client-server protocol works by the client initiating a connection with the server and then the server validating whatever login credentials are provided. Once everything is validated the server opens an FTP session
	- An FTP session is created and operates over two channels
		### A Command Channel
		- A command channel is as it's name implies, it is the channel through which commands and replies to commands are sent. 
		### A Data Channel
		- A data channel is also as it's name implies, it is the channel through which data (files) are sent. Whoever made FTP is the best at naming things in all of Computer Science.
- FTP servers may support either/both
	## Active Connections
	- An active channel is when the client opens a port and listens which the server is required to actively connect to, like a [[Basic Cybersecurity Terms#Reverse Shell]].
	## Passive Connections
	- A passive channel is when the server opens a port and listens and the client connects to it like a [[Basic Cybersecurity Terms#Local Shell]].
- To connect to a server over FTP simply use the syntax ftp \<ip\>
- Files can be retrieved or added to the FTP server using API language
For information on how to exploit FTP go to [[FTP Hacking Tools]]