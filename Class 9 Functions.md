# Advanced concepts
Link to original page: [here](https://python.land/deep-dives/functions)
## Forced keyword arguments
- Creates better clarity especially in the case of debugging
- for long list of args it is sometimes better to make a dictionary with all the named arguments
## Decorating functions
- #decorators are wrappers around a function that modify the behavior of the function in a certain way
- EX:

```
def print_argument(func):
     def wrapper(the_number):         
	 print("Argument for", func.__name__, "is", the_number)
	 return func(the_number)      
	 
	 return wrapper  
@print_argument
def add_one(x):     
	return x + 1
	  
print(add_one(1))

```
- Inside the `print_argument` the wrapper function is defined
## Anonymous functions
- Sometimes naming a function is not worth the work (like if the function is only going to be used once)
- A lambda function can be assigned to a variable creating a concise way of defining a function
## Function calling: Partials
- These are templates for how a function is called