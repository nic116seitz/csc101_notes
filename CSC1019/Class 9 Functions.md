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

Second reading for [Advanced function Calling](https://dev.to/cwprogram/advanced-function-calling-in-python-272j)
## Function calling: Partials
- These are templates for how a function is called
- This is useful in the case where you would create a function to call another function, this eliminates the need for caller functions
## Dynamic Keyword Args
- Useful for building up values to pass on
## Function mapping
- Allows you to create a list of function calls
## Dynamic Method Calling
- Methods are essentially attributes of a class or class instance
- For static methods bound to the class itself getattr can be used with class and method name

Resource for [Number systems in Python](https://www.geeksforgeeks.org/python/number-system-in-python/) 
## Number systems in Python
- The writing system for denoting numbers logically using digits or symbols is defined as a #Number_System
- It is a system that defines numbers in different ways
#### Types of numbers system
- Four main types
- Binary base 2 
- Octal base 8
- Decimal base 10
- Hexadecimal base 16
### Binary Number system
- 