<h1>Mutable objects as default parameters</h1>

It turns out that default parameter values are evaluated once.

After you have declared a function, a new object for a default value is created. 
It will be used from this point on. This means that if the function modifies 
this object in some way, the default value in the mutable will change too. 
For this reason, you should use mutable default values carefully.

Here is a common workaround to fix the function from our earlier example:
```python
def add_player(player, team=None):
    if team is None:
        team = []
    team.append(player)
    return team
```
Setting the default value to None and explicitly reassigning the value of the 
team parameter allows you to create a new list each time this function is 
called.