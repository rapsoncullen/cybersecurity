- To be able to replace something within a view in django do the following
	- Put the contents to replace within curly brackets 
		- ex. \<h1\>Hello, {name}\<h1\>
	- Pass in the context to the HttpResponse() method
		- ex. 
```Python
from django.http import HttpResponse
from django.template import loader
def home(request):  
	context = {"name": "Junior"}  
	template = loader.get_template("app/home.html")  
	return HttpResponse(template.render(context))
```
