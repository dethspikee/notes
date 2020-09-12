<h1>Django Views</h1>

A view is a Python callable (usually function or class) that receives a 
HttpRequest and returns HttpResponse. Inside the view we handle all our logic 
and generate a webpage. Django ‘view’  maps to a Controller in the MVC model. A 
web page consists of data and url configuration. Url configuration is a list of 
url patterns that Django uses to know which view to use for request. 

Django removes the first ‘/’ root slash and then tries to match the remaining 
of the path with our url patterns. 

When a user types an address in their browser, their browser will look up the 
network location and then find out the scheme and path and send HTTP request to 
that location. Django will take that request, map it into a Python object 
‘HTTPRequest’ and send it to the appropriate view that will return HttpResponse.

We can use standard view functions or class based views. 

Class based views inherit from ‘View’ class. They are compliant with HTTP 
methods meaning that inside of CBV developers have to create methods such as 
get, post, put in order to handle all types of requests. If a POST request comes 
but the post method is missing, the user will see 405 error - method not found.

Meanwhile view functions are not HTTP compliant meaning that if post method is 
not handled by a developer, the request will be handled as a GET method and the 
user won’t see ‘Method not allowed’ message, unless a specific decorator was 
used. 
