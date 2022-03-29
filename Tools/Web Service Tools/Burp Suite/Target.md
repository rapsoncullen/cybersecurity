- The Target in Burp Suite allows you to define your [[Basic Cybersecurity Terms#Scope]], view a site map, or specify issue definitions. 
- When starting a web application test youll likely be provided a few things
	- The application URL
	- A list of the different user roles within the application
	- Various test accounts and associated credentials for those accounts
	- A list of pieces/forms in the application which are out of scope for testing and should be avoided
- Make sure to set your scope so that you do not cause harm to the website or access anything that isn't meant to be accessed.
- There are three options for the Target, Site Map, Scope and Issue Definitions
## Site Map
- Once you have gone through the [[Proxy#Intercept]] step of enumeration the websites you have intercepted will be on the left hand side of the Site Map. Right clicking on any of these options will bring up all sorts of actions but the most important one is on top "add to scope"
## Scope 
- All things you have added to Scope will be here
## Issue Definitions
- This has all of the possible issues Burp Suite defines within reporting. This can be useful for understanding and categorizing various findings.