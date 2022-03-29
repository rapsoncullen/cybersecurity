- XML or Extensible Markup Language is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. It is used for storing and transporting data. It comes with the following advantages
	- XML can be used for any system and supports the technology change when transferred from one system to another.
	- The data can be changed at any point without impacting the data presentation.
	- XML allows validation using [[#DTD or Document Type Definition]] and Schema which makes sure it is free from any syntax error.
	- XML simplifies data sharing between various systems because of its platform-independent nature. 
- Every XML document mostly starts with what is known as XML Prolog that typically looks like so
	- \<xml version="\<version number\>" encoding="\<encoding format\>"?\>
- Every XML document must contain a 'ROOT' element that typically adheres to the following syntax

		<mail>  
		   <to>falcon</to>  
		   <from>feast</from>  
		   <subject>About XXE</subject>  
		   <text>Teach about XXE</text>  
		</mail>`
## DTD or Document Type Definition
- The DTD defines the structure and the legal elements of an XML document. It adheres mostly to the following syntax
	- \<!DOCTYPE \<doctype\> \[ \<!ELEMENT \<element\> (\<all of the sections of the 'ROOT' element\>) \<!ELEMENT]  (((To Be continued, don't know enough about XML to honestly flesh out the syntax)))
- !DOCTYPE defines a 'ROOT element'
- !ELEMENT defines an element