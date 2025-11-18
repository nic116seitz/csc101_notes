# Intro
## Grouping related items into objects
- Classes are groupings of lower level objects
- Think var and functions
- #object is a grouping of data and vars and operations that can be performed on said data
## Abstraction/Information hiding
- #abstraction occurs when a user interacts with an object at a high level, allowing lower-level internal details to remain hidden #information_hiding or #encapsulation 
- Objects support abstraction by hiding entire groups of functions and vars and exposing only certain functions to the user
- #abstract_data_type is a datatype whose creation and update are constrained to specific well-defined operations
## Python built-in objects
- Python automatically creates #built-in objects for programmer to use this includes basic data types like integers and strings
# Grouping Data
- Multiple vars are frequently related and should be treated as one variable with multiple parts
- #class keyword can be used to create a user-defined type of objects containing groups of related vars and functions
- #object maintains a set of #attributes that determines the data and behavior of the class
- #instantiation operation is performed by "calling" the class, using parentheses like a function 
- An instantiation operation creates an #instance, which is an individual object of the given class.
- This instantiation automatically calls the \_\_init\_\_ method defined in the class definition
- #method is a function defined within a class
- #init method, commonly known as a #constructor is responsible for setting up the initial state of the new instance
- \_\_init\_\_ is responsible for setting up the initial state of the new instance
- the init method has a single parameter self that automatically references the instance being created

# Classes
From [Python Docs](https://docs.python.org/3/tutorial/classes.html)
- Each instance of a class can have attributes attached to it for maintaining its state
- Class instances can also have methods
- Class instances can also have methods (defined by its class) for modifying state
- They can be modified further after creation
## Names and Objects
- Objects have individuality and multiple names (in multiple scopes) can be bound to the same object #aliasing
- Aliasing behave like pointers in some respect
	- Ex: passing an object is cheap since only a pointer is passed by the implementation; and if a function modifies and object passed as an arg the caller will see the change

## Python Scopes and Namespaces
- #namespace is a mapping from names to objects, most namespaces are currently implemented as dicts
- #attribute is any name following a dot
- names in modules are references to attributes (think builtin such as key or value in the case of dicts)
- Module attributes are writable 
	- Ex: `an_object.attribute = attribute_assignment`
- Writable attributes may also be deleted with the del statement
	- Ex: `del an_object.attribute` will remove `attribute_assignment`
- Namespaces are created at different moments and have different lifetimes
	- builtin names is created when the python interpreter starts up and is never deleted
	- global namespace for a module is created when the module definition is read
	- module namespaces also last until the interpreter quits
	- local namespace for a function is created when the function is called and deleted when the function returns or raises an exception that isn't handled
- 