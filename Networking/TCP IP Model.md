- The TCP\/IP model is very similar to the OSI model only a few years older.  The TCP\/IP model is what is typically used for real world networking and it only has four layers

# The Four Layers
## Application
- Combines [[The OSI (Open Systems Interconnection) Model#Application]] + [[The OSI (Open Systems Interconnection) Model#Presentation]] + [[The OSI (Open Systems Interconnection) Model#Session]] layers
## Transport
- Works roughly the same as the [[The OSI (Open Systems Interconnection) Model#Transport]] layer
## Internet
- Works roughly the same as the [[The OSI (Open Systems Interconnection) Model#Network]] layer
## Network Interface
- Combines [[The OSI (Open Systems Interconnection) Model#Data Link]] + [[The OSI (Open Systems Interconnection) Model#Physical]]

# Protocols
- While it is nice to think of TCP\/IP as a layered approach at the end of the day it is a long series of protocols, the two most important of which are [[The OSI (Open Systems Interconnection) Model#TCP]] and IP
## TCP continued \(The Three Way Handshake\)
- TCP relies on what is called a three way handshake to establish a connection between two machines and then make that connection as seemingly lossless as possible. This three way handshake goes as follows
	- The client sends a request to the server called a SYN (synchronize) bit
	- The server respnds with an ACK (acknowledgement) bit and it's own SYN bit
	- The client responds to the server's SYN bit with an ACK bit