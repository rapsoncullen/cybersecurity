# [[SMB]] access tools
## smbclient
- smbclient comes packaged with kali linux and lets you access SMB shares
- Basic syntax is smbclient \/\/\<ip\>\/\<share\> -U \<user\> -p \<port\>
- To download or upload file from smb use API terms like get or post
# SMB enumeration tools
## enum4linux
- enum4linux is a tool that puts a wrapper around the tools in the samba package making it easy to extract information from the target pertaining to smb
- Basic syntax is enum4linux \<tag\> 
	- Most useful tag is -A which just goes through everything you need