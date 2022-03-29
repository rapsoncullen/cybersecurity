- Cookies are small bits of data that are stored in your browser. Each browser will store them seperately so they are not cross platform. The most common reason for cookies is for **advertisements** and are typically sent with each [[HTTP Requests]] made to a server and is set by the [[HTTP Request Headers#Set-Cookie]] typically with the syntax that follows.
	- Set-Cookie: \<  \<cookie-name\>  \>=\<  \<cookie-value\>  \>
- Since HTTP is stateless and doesn't keep track of anything sites will use cookies to track any information they need to about your experience, such as what items are in your shopping cart.
- With each request to the server it will typically send back all of your cookies using the [[HTTP Request Headers#Set-Cookie]]
- There are two main types of cookies, session cookies and permanent cookies
## Session Cookies
- Cookies that are deleted upon the session ending
## Permanent Cookies
- Cookies that are deleted at a time set by the **Expires** attribute or the **Max-Age** attribute
# Cookie Destination
- The scope of a cookie is set by the **Domain** attribute and the **Path** attribute and the security of the delivery is maintained by the **SameSite** attribute.
## Domain
- The **Domain** attribute specifies which hosts are allowed to receive the cookie. If unspecified it defaults to the same host that set the cookie, excluding subdomains.
	- If **Domain** is specified then subdomains are always included.
- Specifying **Domain** actually makes a cookie less restrictive
## Path
- The **Path** attribute indicates a URL path that must exist in the requested URL in order to send [[HTTP Request Headers#Cookie]]
## SameSite
- The **SameSite** attribute lets servers specify whether/when cookies are sent with cross-site requests. This provides some protection against [[Basic Cybersecurity Terms#CSRF]]
- **SameSite** takes three possible values, Strict, Lax and None
	- Strict
		- The cookie is only sent to the same site as the one that originated it
	- Lax
		- The cookies are sent when the user navigates to the cookie's origin site
	- None
		- The cookies are sent on both originating and cross-site requests but only if the **Secure** attribute has been set.

# Cookie Vulnerabilities
## Not Restricted By Default
- Cookies by default are not restricted and are easily accessed by a [[Basic Cybersecurity Terms#Man-In-The-Middle Attack]]. They can however be secured using either the **Secure** attribute or the **HttpOnly** attribute
	- The **Secure** attribute is sent to the server only with an encrypted request over HTTPS never with unsecured HTTP. Servers with HTTP in the url can't use the **Secure** attribute
	- The **HttpOnly** attribute makes the cookie inaccessible to the Javascript Document.cookie API so that it is sent only to the server. [[#Permanent Cookies]] should almost always have the **HttpOnly** attribute. This helps mitigate [[Basic Cybersecurity Terms#XSS]]
## No Location
- The design of the cookie mechanism makes it so that a server is unable to confirm that a cookie was set on a secure origin or even to tell where a cookie was originally set at all.
- If you have one vulnerable application on a subdomain it can set a cookie with the **[[#Domain]]** attribute and get access to that cookie on all other subdomains. This can be abused in a [[Lesser Known Attacks#Session Fixation]] attack.
- This vulnerability is typically solved using two prefixes, __Host and __Secure.
	- __Host
		- If a cookie has the host prefix it has plenty of restrictions on it to help prevent an attack, these include as follows
			- It can only be set if it is also marked with the **Secure** attribute
			- It can only be set if it was sent from a secure origin
			- It can only be set if it does not include a **[[#Domain]]** attribute
			- It can only be set if the **[[#Path]]** attribute is set to '/'
		- With all of this in mind cookies with the Host prefix can be seen as domain locked.
	- __Secure
		- If a cookie has the secure prefix it only has the restrictions that it is marked by the **Secure** attribute and was sent from a secure origin.
- 