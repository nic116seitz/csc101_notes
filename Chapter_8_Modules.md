# Module Basics
## **Modules**
- Code that runs one line at a time is generally used when writing code for short programs, (for practicing syntax)
- Programmers typically write Python program code in a file called a #script
- The script is then passed into a python interpreter
- Collections of logically related code can be stored in separate files and imported for use into a script that requires said code
- Modules are made available for use via an import statement
- Once imported any object defined in that module can be accessed using #dot_notation
	- Ex: A variable `speed_of_light` defined in `universe.py` is accessed via `universe.speed_of_light`
- Separating code into different modules makes management of larger programs simpler
- Python standard library is a collection of pre-installed modules.

| Term          | Definition                                                                                                        |
| ------------- | ----------------------------------------------------------------------------------------------------------------- |
| #Script       | A file containing Python code that is passed as input to the interpret                                            |
| #Module       | A file containing Python code that is imported by a script, module, or interactive interprerter                   |
| #dot_notation | Used to reference an object in an imported mo                                                                     |
| #import       | To execute the contents of a file containing Python code and make available the definitions from that filet  ilet |
## **Importing modules and executing scripts**
- When module is imported all code in the module is immediately executed.
- Python programs often use the built-in special name \_\_name\_\_ to determine if the file was executed as a script by the programmer or imported by another module
## **Functions**
**General**
- To reduce redundancy statements can be grouped to create repeating operations known as a #function 
- #function_definition consists of the function's name and a block of statements
- #function_call is an invocation of the function's name causing the function's statements to execute
- Examples of builtin functions are input(), in(), len(), etc
- *def* is the keyword that is used to create new functions
## Return statements
- A function may return one value using a #return_statement
- A function can only return one item
- A function with no return statement returns the value #None 
- #None indicates no value 
## Parameters
- #parameter is a function input specified in a function definition
- #argument is a value provided to a function
	- Ex:
	- ```
	  func_name(x1,x2)
	  # x1 and x2 are parameters
	  func_name(2, 4)
	  # 2 and 4 would be arguments
	  ```
### Multiple or no parameters
- a function may have multiple parameters separated by commas 
- Or a no parameters simply `def` followed by `function_name` followed by `()` 
	- Ex: `def my_function()`
## Printing from a function
- A function with no return statement is called a #void_function and such a function returns the value #None 
## Calling a print function multiple times
- complex output statements can be written in code once
- functions can then be called multiple times to produce the output instead of rewriting the statements
# Dynamic Typing
## Dynamic and static typing 
- A programmer can pass any type of object as an argument to a function
- #polymorphism is the function's behavior of adding different types together
- Python uses #dynamic_typing to determine the type of objects as a program executes
	- (the type of an object can change based on context)
- in #static_typing languages the type of each variable and every function parameter in a program's source code is defined
# Reasons for defining functions 
- Decomposing programs into functions can help with program readability
- Makes a program more maintainable in the future 
## Modular program development
- #Modular_development is the process of dividing a program into separate modules that can be developed and tested separately and integrated into a single program
- function stubs are used to capture the high-level behavior of required functions before diving into the details of each function
**Avoid writing Redundant code**
- A function can be defined once then called from multiple places in a program, thus avoiding redundant code.

# Writing mathematical functions
## Mathematical functions
- A function is defined as a mathematical calculations involving several numerical parameters and returning a numerical result
##### Calling functions in expressions
- A function call evaluates to its returned value
# Function Stubs
## Incremental development and function stubs
- #incremental_development is when small amounts of code is written and tested then a small amount more is written and tested and so on
- #function_stubs are a part of this process
	- function definitions whose statements haven't been written yet
	- This is for capturing the high-level behavior before writing the actual function
	- One way to use these is by using the #pass keyword which performs no operation except to act as a placeholder for a required statement
	- Another alternative is to use print statements for function stubs so you know when the program has reached the function
	- If the programmer wants to stop the program to stop when the function is called the they can use `raise NotImplementedError` This will cause the program to terminate when it reaches the function

# Lists basics
## Creating a list
- A #container is a construct used to group related values together and contains references to other objects instead of data
- A #list is a container created by surrounding a sequence of variables or literals with square brackets
- lists are sequences contained elements are ordered by position in the list
	- position in a list is known as #index
## Accessing list elements
- Lists are useful for reducing the number of variables in a program. Instead of having a separate variable for the name of every student in a class for every word in an email, single list can store an entire collection of related variables 
- Individual  list elements can be accessed using an indexing expression
	- EX: `my_list[3]`
	- This would access the third element of a list
- A list's index must be an int
- non int will terminate a program
- Lists are mutable meaning that elements of a list can be accessed and changed
## Adding and removing list elements
- #method instructs an object to perform some action and is specified by providing the object name followed by a "." and then the method name
-  the `append()` list method is used to add new elements to a list
- Elements can be removed from a list using the `pop()` or  `remove()`
## Sequence-type methods and functions 
- Methods like `append()`, `pop()`, and `remove()` are sequence type methods
- #sequence-type_methods are functions that are built into python language definitions of sequence types liek lists and strings. 
	- These typically alter or return some information about the object
- #Sequence-type_functions are functions built into python that take sequences as arguments and operate on the sequences

### Some of the functions and methods useful to lists

| Operation         | Description                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------- |
| `len(list)`       | Find the length of the list.                                                                 |
| `list1 + list2`   | Produce a new list by concatenating list2 to the end of list1.                               |
| `min(list)`       | Find the element in the list with the smallest value. All elements must be of the same type. |
| `max(list)`       | Find the element in the list with the largest value. All elements must be of the same type.  |
| `sum(list)`       | Find the sum of all elements of a list (numbers only).                                       |
| `list.index(val)` | Find the index of the first element in the list whose value matches val.                     |
| `list.count(val)` | Count the number of occurrences of the value val in the list.                                |

# Functions: Common errors
## Errors
- Copying a function to convert C to F but forgetting to change the print statement to match
- Return errors
	- Failing to return a value for a function 
	- Failing to change what the function should be returning
# Scope of variables and functions
## Variable and function scope 
- Variable or function object is only visible to a part of program known as #scope 
- If var created in function it only exists in the function it was created in
- variables created in functions are called local variables
## Global Variables
- vars defined outside of function are called global variables
- scope extends from assignment to end of the file
- `global` must be used to change the value of a global variable inside of a function
# Namespaces and scope resolution
## Namespace
- #namespace maps names to objects
- when executing assignment the interpreter looks in the namespace to find the values of referenced variables
## Scope and scope resolution
- #scope is the area of code where a name is visible
- Each scope such as global scope or a local function scope has its own namespace
- At least three nested scopes are active at any point in a programs execution 
	- Builtin scope: Contains all the builtin names
	- Global scope: Contains globally defined names outside of any functions
	- Local scope: The scope currently executing
- if an name cannot be found in any scope this generates a `NameError`
- The process of searching for a name in the available namespace is called scope resolution
# Function args
## Function args and mutability
- Args to funcs are passed by object reference #pass-by-assignment
- When a func is called new local variables are created in the function's local namespace by binding the names in the parameter list to the passed args 
- If obj being modified is immutable such as str or int then modification is limited to inside the function
	- modification in this case results in the creation of a new object
- If obj is mutable then in place modification of the object is seen outside the scope of the function 
	- Ex: adding elements to a container or sorting a list that is performed within a function will also affect any other var in the program that reference the same object