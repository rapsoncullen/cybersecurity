- NFS or Network File System allows a system to share directories and files with others over a network. Unlike with [[FTP (File Transfer Protocol)]] or [[SMB]] NFS allows you to access these files as if they were local instead of simply transferring them. 
- Here is the NFS documentation https://docs.oracle.com/cd/E19683-01/816-4882/6mb2ipq7l/index.html
- NFS works as follows
	-  First the client requesting to mount a directory from a remote host on a local directory the same way it would mount a physical device. It will then connect using [[RPC (Remote Procedure Call)]]
	-  The server then checks if the user has permission to mount whatever directory has been requested. It will then return a file handle to identify it.
	-  If someone wants to access a file using NFS an RPC call is placed to the daemon for NFS. This call takes parameters such as
		-  The file handle
		-  The name of the file to be accessed
		-  The user's user ID
		-  The user's group ID
-  NFS is mostly used to access files crossplatform somewhat easily
-  NFS is typically accessed through NFS-Common
## Root Squashing
- NFS by default has a process called Root Squashing enabled which prevents anyone from connecting to the NFS share from having root access to the volume. Remote root users are actually assigned a user named "nfsnobody" which has the least local privileges.
For information how to exploit NFS go to [[NFS Hacking Tools]]