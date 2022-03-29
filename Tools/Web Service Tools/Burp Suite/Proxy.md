- Proxy works similarly to all other proxies, it allows us to relay out traffic through an alternative route to the internet only instead this time it's going through Burp Suite.
- Proxy has four main options which are as follows
## Intercept
- Intercept should almost always be your first step on the whole Burp Suite project. This is the tool which allows you to intercept traffic from your browser in order to enumerate it.
- Intercept has four important options, forward, drop, intercept, and action
	- Forward 
	- Drop 
	- Intercept turns Intercept on or off
	- Action gives you a whole host of options such as sending the information over to the [[Repeater]]!
## HTTP history
- HTTP history is used for accessing all [[HTTP Requests]] that have been intercepted. Very useful for enumeration
## WebSockets history
- WebSockets history is used for access all WebSockets that have been intercepted.
## Options
- Options in proxy aren't just your standard ability to apply cosmetic changes. Options in Burp Suite Proxy is where you set up your browser as a proxy listener, intercept client requests and so much more
	#### Intercept Client Requests
	- The Intercept Client Requests option in the options section of Burp Suite  proxy allows you to decide exactly what requests will be intercepted and stored by the proxy that it wouldn't by default. By default the only one of these that is turned on is the one that intercepts files. Once you have gone to the domain of the target you should enable the rule here that sets the scope as the currently intercepted url
	#### Response Modification
	- The Response Modification option in the option section of Burp Suite proxy allows you to automatically modify responses you get from the proxy. This can be everything from enabling disabled form fields to removing all javascript form validation. Or even removing all javascript!
	#### TLS Pass Through
	- The TLS Pass Through option in the option section of Burp Suite proxy allows you to choose web servers that won't have any of their requests or responses available in the proxy intercept view or history. 
	- Useful for keeping you in scope