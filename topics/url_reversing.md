<h1>URL Reversing</h1>

We can build an url path by doing a URL reverse (using ‘reverse’ function or ‘url’ functionality in templates). 
We can provide a name of our URL pattern and django will try to match its URL pattern in order to create a URL path. If our path required extra arguments we can pass extra information to our reverse function like this:

reverse(‘nameOfURLPattern’, kwargs={‘argument’: value}

We can also use get_absolute_url method on our model to create a unique URL path for each model instance that we can later refer to in our templates.
