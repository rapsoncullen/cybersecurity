# Important Switches
## David Bowie
- self explanatory
## -sS : Syn Scan or Stealth Scan
- A stealth scan works by first trying to engage in a [[TCP IP Model#TCP continued The Three Way Handshake]] but then instead of fully connecting it sends a RST flag to the server instead of the final ACK bit.
- Stealth scans are no longer typically stealthy. On older machines their intrusion detection servers weren't set up to look for this type of connection but newer machines are well aware of this tactic.
- Stealth scans are significantly faster than TCP connect scans
## -sU : UDP Scan
- UDP scans are much harder to rely on because of the way [[The OSI (Open Systems Interconnection) Model#UDP]] works. Since UDP doesn't wait for a response NMAP will just assume that the port is open if it doesn't respond with a denial. However this means NMAP won't be able to tell the difference between open ports and ports behind a firewall.
## -sT : TCP Connect Scans
- TCP Connect Scans work by trying to engage in a [[TCP IP Model#TCP continued The Three Way Handshake]] with each port. If the port is closed the target server will respond with a RST flag instead of a SYN/ACK flag.
## -sN : TCP Null Scans
- TCP Null Scans try to scan ports by sending TCP requests with **no flags at all**. As per RFC the target host should immediately respond with a RST if the port is closed. 
- TCP Null Scans are seen as far more stealthy than typical scans
- Used in firewall evasion because computers may not be dropping TCP packets that don't have the **SYN** flag set
## -sF : TCP FIN Scans
- TCP FIN Scans try to scan ports by sending TCP requests with the **FIN** flag which as per RFC the target should immediately respond with a RST if the port is closed.
- TCP FIN scans are seen as far more stealthy than typical scans
- Used in firewall evasion because computers may not be dropping TCP packets that don't have the **SYN** flag set
## -sX : TCP Xmas Scans
- TCP Xmas Scans try to scan ports by sending a mangled TCP request which as per RFC the target should immediately respond with a RST if the port is closed.
- TCP Xmas Scans are named after how they look in wireshark which is similar to a blinking christmas tree.
- Microsoft Windows will often mess up this scan by responding to all mangled TCP requests with a RST breaking RFC
- Used in firewall evasion because computers may not be dropping TCP packets that don't have the **SYN** flag set
## -O : Operating System Scan
## -sV : Version Scanning
## -v : Verbose Scanning
- -v : Verbose Scanning is used to make sure you get all information you might need about each port. It doesn't cut off **most** of the fluff from what you are asking NMAP
## -vv : Extra Verbose Scanning
- -vv : Extra Verbose Scanning is for when you need NMAP not to cut out **any** of the fluffy from what you are asking it

## -oA : Output results in major formats
- -oA : Ouptut results in major formats does just what the heading implies. It outputs the results in normal, xml and greppable format.
## -oN : Output results in normal format
## -oG : Output results in greppable format
## -A : Enables "Agressive" mode
- Agressive mode is the loudest NMAP gets, pushing for service detection, operating system detection, a traceroute and common script scanning
## -t\<1-5\> : Speed
- -t\<1-5\> sets just how fast the detection will go, keep in mind the faster you choose the more errors you can expect and the louder you will be.
## -p \<port number\> : Chooses specific ports to scan
## -sn \<IP address or range\> : Do not scan any ports
- Why would you not want to scan any ports? To perform a ping sweep which creates a map of all devices on a network.
## -Pn : Do not bother pinging the host before scanning it
- Windows Firewalls by default block all ICMP packets which is what we typically use to establish the activity of a target, -Pn treats the target as always being alive which bypasses this block.
## -f : fragment packet
- Firewalls have a harder time detecting packets when they are in smaller pieces, -f allows us to split our packet up as small as possible.

### --top-ports \<number\> : Scans the most common ports
### --mtu \<multiple of 8\> : Sets a max size for packets sent
### --scan-delay \<time\>ms : adds a delay between packets sent
- Useful for dealing with time-based Firewall/IDS triggers that may be in place.
### --badsum : sends an invalid checksum for packets
- Helps you to determine the presence of a firewall/IDS because they will respond automatically while a real TCP/IP stack would drop this packet.
### --data-length \<number\>: attaches an arbitray length of random data to the end of packets
