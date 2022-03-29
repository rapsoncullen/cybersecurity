- [[What is the OWASP Top 10#Cross-site Scripting]] is split into three categories as described in the page [[What is the OWASP Top 10]] and based on those categories it can do some of the following things.
- Basic XSS is done simply by when you know something you input is going to be displayed, putting in a script instead.
## Cookie Stealing
- Cookie stealing is when an attacker steals your [[Basic Cookie Information#Session Cookies]] so that they can log in as you without having to provide authentication.
- The easiest way to do this is by simply having a script that executes that sends "document.cookie"back to the attacker, typically by storing it on a web server the attacker controls.
- the attacker can then use a script that allows them to execute \<script\> document.cookie = (cookie)\<\\script\>
## Keylogging
- An attacker can register a keyboard event listener and send all of your keystrokes to their own server.
- Using the document.onkeypress() function from javascript an attacker can easily tell what keys you are typing and send them their way.
## Webcam Snapshot
- Using HTML5 capabilities it is even possible to take snapshots from a compromised computer webcam
## Phishing
- An attacker could either insert fake login forms into the page or have you redirected to a clone of the site you planned on going to.
## Port Scanning
- Stored XSS can be used to scan an internal network and identify other hosts on their network. 
- The way this would typically be done is by requesting an image from all ips on a given host's network that would almost certainly be available on something like a web server.
## Other

## Common Filters
- Filtering out script tags
	- Simply place the script instead in another html element and use something like "onclick"
# Forms of Protection
## Escaping
- Escaping escapes all user input. This means any data your application has recieved is secure before rendering it for your end users. A common way to do this is to prevent any dangerous characters such as \< and \> from being rendered in the first place. 
## Validating Input
- This is the process of ensuring your application is rendering the correct data and preventing malicious data from doing harm to your site, database, and users. It does this by disallowing certain characters from being inputted in the first place such as \< and \>
## Sanitising
- Sanitising user input is a strategy that should never done alone but it can be useful. Sanitising is when you change unnaceptable user input into an acceptable format such as changing the < character into the HTML entity &#60

# Resources
- One of your best friends with XSS is http://www.xss-payloads.com/payloads-list.html?a#category=all
- BeEF is a useful tool we will learn more about later, it is located right now in Downloads/beef and can be opened by using ./beef