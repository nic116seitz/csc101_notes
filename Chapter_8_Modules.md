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
| #Module       | A file containing Python code that is imported by a script, module, or interactive interpre                       |
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
- 