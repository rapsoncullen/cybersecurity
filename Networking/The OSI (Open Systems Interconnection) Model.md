While most modern systems use the TCP/IP model the OSI model is still useful to know. It is comprised of seven layers

# The Seven Layers
## Application
	- The application layer is what provides networking options to programs running on the computer, providing an interface for them to use in order to transmit data. When data is given to the application layer, it is passed down to the presentation layer
## Presentation
	- The presentation layer is where any data from the application layer is transformed into whatever form it needs to be. This could either mean it came from an application that gave the data in a non-standardized format and it needs to make it more readable for whatever is receiving it, or it could mean encrypting the data to keep it from being read by people it isn't supposed to be read by.
## Session
	- Once the session layer receives data from the presentation layer it is it's job to open a session with the other computer across the network. If this isn't possible then an error is thrown and the process gets no further. Once a session is open it must remain open for active communication between the computers.
## Transport
	- The transport layer determines the protocol over which the data is to be transmitted and then divides up the transmission into bite sized pieces for tranzit.
	- The transport layer typically picks one of two protocols, TCP or UDP	
#### TCP
	- TCP stands for Transmission Control Protocol. This protocol creates a connection between two hosts that is maintained throughout the duration of a request. This allows to make sure all data gets to it's target in tact and if it doesn't it can be resent. This is best used for situations that need accuracy such as a webpage
For further information see [[TCP IP Model#TCP continued The Three Way Handshake]]
#### UDP
	- UDP stands for User Datagram Protocol. This protocl basically just chucks data at the receiving computer as fast as possible with little care for accuracy. This is best for situations where a few lost bytes doesn't matter but a lot of data has to be transferred such as with video streaming.
	- If a UDP connection can't be made on that port, the server will send back a ping on ICMP to say that it is unreachable
## Network
	- The network layer is responsible for locating the destination of your request. This is mostly done by locating the IPV4 of the machine you are trying to communicate with.
## Data Link
	- The data link layer focuses on the physical addressing of the transmission. It takes the packet from the network layer and then adds in a MAC address. It also checks data to make sure it hasn't been corrupted during transmission.
## Physical
	- The physical layer is what turns all of this transported data into binary and then actually moves it across the network.
	
# Encapsulation
	- Each step of the 7 layers a different piece is added onto the data. Also at steps 5,6,7 the name of the data changes because of this addition.
	
![](https://muirlandoracle.co.uk/wp-content/uploads/2020/02/image.jpeg)

