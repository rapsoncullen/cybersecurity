- Metasploit is about the most powerful tool you will ever use in cybersecurity. 
- Before you can start using Metasploit you need to initialize the database using the syntax **msfd init**
- Now to start up metasploit you need to use the syntax **msfconsole**
	- You can use the -q tag to keep it from showing the large obvious banner
- The syntax **db_status** will let you check if your connection to the postgresql database is solid
- You can either use the syntax **help** or **?** to activate the help menu
- Metasploit consists of six core modules which are as follows
# Metasploit Modules
## Exploit
- The Exploit Module is the most commonly used module. It contains all of the exploits (shocker) for you to look up. If you find out the version of a software being run it is smart to look it up in the Exploit Module to see if it has any known exploits.
## Payload
- The Payload Module is the next step after proper enumeration. The Payload Module has all of the Payloads (shocker) for you to arm and aim at a target once you realize the proper exploit. 
## Encoder
- The Encoder Module is the possible next step after choosing your payload. The Encoder Module is used to change the "appearance" of our exploits such that we can avoid detection.
## NOP
- The NOP module is used for buffer overflow and ROP attacks
## Auxiliary
- The Auxiliary Module is used for enumeration. It is most commonly used for scanning a machine and verifying it is exploitable.
## Post
- The Post Module is used for [[Basic Cybersecurity Terms#Looting and Pivoting]] and can be read about more in [[Post Modules]]

- Not all modules are loaded by default. In order to load different modules make sure to use the [[Important Metasploit Commands#Load Loads in different Basic Metasploit Metasploit Modules]] command

# Other Tools In Metasploit
## NMAP
- NMAP is available in metasploit through the use of the [[Important Metasploit Commands#db_nmap Lets you run Basic NMAP in metasploit]] command. Not only this but Metasploit gives it even **more** functionality
	- If you run NMAP in metasploit it saves all ports and the services that were on them as well as any vulnerabilities found in enumeration. To access these use the commands found under [[Important Metasploit Commands#db_nmap Lets you run Basic NMAP in metasploit]]
# Using a payload
- To pick a payload simply search it up and use the syntax use
- For most payloads you are going to want to first use the syntax \<show options\> and make sure you have everything filled in. Once that is done you want to simply use the syntax exploit or run -j