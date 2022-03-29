- SSH is used to create a connection between two machines that allows a client to operate commands on a server. It is protected by a strong key typically named id_rsa.
- Basic syntax for using ssh is 
	- If you have a key file
		- ssh -i \<key-file\> \<username\>@\<ip\>
	- If you don't have a keyfile
		- ssh -l \<username\> \<ip\>