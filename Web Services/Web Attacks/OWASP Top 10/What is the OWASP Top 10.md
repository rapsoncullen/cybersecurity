# Injection
- Injection flaws are when user controlled input is interpreted as actual commands. This can take a handful of forms such as SQL injections or Command Injection. These happen when user input is passed to sql queries and when user input is passed to system commands respectively.
- The main defense against this type of attack is having an allow list. This makes it so that when input is sent to the server it is compared to a list of safe input or characters. If the input is safe, then it is processed. Otherwise it is rejected and the application throws an error.
- If the input contains dangerous characters these characters are removed before they are processed.
# Broken Authentication
- Authentication is essential to modern web applications. Due to just how interconnected modern markets are with our everyday web use it is essential for most websites to have solid ways of authenticating users, typically through a username and password system.
- Since [[HTTP Requests]] are stateless the server must provide [[Basic Cookie Information#Session Cookies]] in order to verify the user. Once a server has attached a session cookie it can keep track of a users' actions.
- If an attacker is able to find a flaw in an authentication mechanism they can exploit this to gain access to other users' caccounts. The most common attacks are as follows
	- Brute Force Attacks
		- If a web application uses usernames and passwords an attacker is able to launch brute force attacks that allows them to guess the username and passwords using multiple authentication attempts. Typically with a tool like [[Basic HYDRA]]. To try to prevent this make sure to have set a lockout for different users after a certain number of attempts.
	- Use of weak credentials
		- A web application should always set strong password policies. If it allows weak passwords like 'password1' it is dooming it's users.
	- Weak Session Cookies
		- If a session cookie uses predictable values an attacker can set their own session cookies and access users' accounts.
- A popular way to help deal with Broken Authentication is Multi Factor Authentication.

# Sensitive Data Exposure
- When a webapp accidentally divulges sensitive data such as names, dates-of-birth, financial information, etc. This is often done through a [[Basic Cybersecurity Terms#Man-In-The-Middle Attack]] where the man in the middle takes advantage of weak encryption of any transmitted data.
- Some websites store their data in what are referred to as [[Basic Cybersecurity Terms#Flat-File Database]] which are easier to set up but also incredibly dangerous because of how easy they can be to access.
# XML External Entity
- An XML External Entity or XXE attack is a vulnerability that abuses features of XML parsers/data. It is often used by an attacker to interact with any backend or external systems the web application has access to. They can also perform Denial of Service attacks or could be used to perform Server-Side Request Forgery which makes the web app make requests to other applications. XXE may even enable port scanning and lead to remote code execution.
- There are two types of XXE attacks
	- In-band
		- In-band XXE attacks are attacks where the attacker can receive an immediate response to the payload. 
	- Out-of-band
		- Out-of-band XXE attacks are attacks where the attacker gets no immediate response so they must reflect the output to some other file or their own server.
# Broken Access Control
- Broken access control is when regular users are able to visit sites that should be protected from them, such as a page to manage other users. This can lead to an attacker being able to view sensitive information or access unauthorized functionality.
# Security Misconfiguration
- Security misconfiguration is just as the name suggests, they occur when there is a security service of library active but it has been inproperly configured. Examples include
	- Poorly configured permissions on cloud services
	- Having uncessary features enabled like services, pages, accounts or privileges
	- Default accounts with unchanged passwords
	- Error messages that are overly detailed and allow an attacker to find out more about the system
	- Not using HTTP security headers or revealing too much detail in the Server [[HTTP Request Headers]]
- This is the most likely vulnerability to lead to more vulnerabilities such as default credentials giving you access to sensitive data, XXE cor command injection on admin pages.
- If you are downloading a file but it will only let you download files with a certain extension you can always put in a Poison Null Byte like %2500 and then the extension that is needed
# Cross-site Scripting
- Cross-site scripting or XXS is an attack that allows the attacker to execute malicious scripts and have it execute on a victim's machine. A website is vulnerable to XSS if it uses unsanitized user input. 
- There are three main types of XSS
	- Stored XSS
		- Stored XSS is XSS that occurs because a malicious string has been placed into a website's database. This typically happens when a website doesnt sanitize user input before it is put into the database.
	- Reflected XSS
		- Reflected XSS is when the malicious payload is part of the victims request to the website. In short this means that the attacker needs to trick the user into clicking a malicious URL which will then perform a dangerous script on their device.
		- A common way to do this is with something like a search bar, where when you type it in it puts whatever you searched for into HTML5 and also changes the url to include the search term. If you search up a script you would then be able to use that URL as an attack
	- DOM-Based XSS
		- DOM-Based XSS is when the malicious payload is placed into the DOM.
# Insecure Deserialization
- Insecure Deserialization has an incredibly broad definition that sounds like it might include other aspects of the OWASP Top 10.
- Inescure Deserialization occurs when untrusted data is able to leverage the serialization and deserialization process used by web applications. 
- There is no reliable tool/framework for this vulnerability yet.
## Serialisation
- Serialization is the process of converting objects used in programming into simpler, compatible formatting for transmission. This is what you would expect the [[The OSI (Open Systems Interconnection) Model#Physical]] layer to do. 
## Deserialisation
- Deserialisation is the process of converting serialised information to their complex form - an object that the application will understand.
# Components with Known Vulnerabilities
- This vulnerability is just as the name suggests, using a component with a known vulnerability. Go to exploit-db for countless known vulnerabilities
# Insufficient Logging and Monitoring
- This is another vulnerability which is just as the name suggests. Every action by the user should be logged and if they aren't then an attacker might go untraced. Not only does not having succifienct logging and monitoring risk future attacks by the same methodology but it also has the possibility to be illegal if you are unable to provide information requested by authorities.
- Logs should store
	- HTTP status codes
	- Time Stamps
	- Usernames
	- API endpoints/page locations
	- IP addresses