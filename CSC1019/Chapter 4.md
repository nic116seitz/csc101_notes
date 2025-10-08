# Programming (general)
## Computer program basics
- Program components
	- #input received data from a file, keyboard, touchscreen, network, etc
	- #process performs data manipulation, computation, etc.
	- #output program puts the data somewhere, like screen network, file, etc.
- Programs use #variables to refer to data
	- This is because the value for a given variable varies as the program assigns the variable with new values
- Program is like a recipe
## Computational thinking
- #computationalThinking is thinking or creating a sequence of instructions to solve a problem,
- #Algorithm a sequence of instructions that solves a problem
## Python Primer
- #pythonInterperter is a computer program that executes code written in the python programming language. 
- An interactive interpreter is a program that allows the user to execute one line of code at a time
- #code is a common word for the textual representation of a program.
- an interactive interpreter displays a prompt that indicates that the interpreter is ready to accept code. 
## Executing a Python program
- #statement is a program instruction. Programs are a series of statements
- each statement sits on its own line
- #expression a piece of code that the interpreter evaluates to produce a value
	- Ex: wage \* hourly
- #assignment the left side (including the equals sign) of an expression
- print() function displays the variable or the expression values
- \# is a comment in python

## Basic input and output
- Each use of print() outputs on a new line
- Sometimes you would want to avoid this
- end=" " at the end of a print statement (inside the brackets)
- Any character can be subbed out for the space inside the quotes
### Moving output to the nextline
- output can be moved to the next line using the newline character
- "\n"
- #escapeSequence is a string that has special meaning, always starts with a \
	- Other examples are \\ to print a \ 
	- \t to insert tab
- tab or newline is #whitespace
##### Basic input
- many useful programs allow a user to enter values such as typing a number, name, etc. 
- input() function is used to read input from a user
	- Ex: ```
	  ```
	  print ("Enter name of best friend:", end=" ")
	  best_friend = input()
	  print("My best friend is", best_friend)
	  ```

#### Converting input types
- strings and integers are each example of #types 
- A type determines how a value can behave
	- Ex: You can divide an int by 2 but it doesn't make sense to do the same with a string
- Reading from input always = string
- When looking to read an int you would wrap your input in a int() function

#### Input prompt
- Adding a string inside the parentheses of input() displays a prompt to the user before waiting for the input and is a useful shortcut to adding an additional print statement
## Errors
### Syntax errors
- #syntaxError violates a programming language's rule on how symbols can be combined to create a program
	- Ex:
		- Multiple print statements on one line
- A good way to avoid writing a lot of errors is to execute code frequently (debug)
### Runtime errors
- #runtimeError means that the program's syntax is correct but the program is attempting an impossible operation
	- Ex:
		- Divide by zero 
		- Non terminating while or if loop
- #runtimeError cause crashes

| Error type       | Description                                                     |
| ---------------- | --------------------------------------------------------------- |
| Syntax error     | The program contains invalid code that cannot be understood     |
| IndentationError | Improper indentation                                            |
| ValueError       | Invalid value used, (think mismatch of types) \\\ int("string") |
| NameError        | variable named doesn't exist                                    |
| TypeError        | An operation uses incorrect types \\\ 9 + apple                 |
a
## IDE (Integrated Development Environment)
##### Intro
- Ide integrates a text editor with a python, in addition to other tools
##### Common features
- Syntax highlighting - uses different colors for keywords variables strings and other code syntax elements
- ***Automatic delimiter completion*** adds matching closing symbol
	- Ex: ( <= is automatically closed with = >)
- Shortcuts for running the program without having to enter a command
- File manager
##### Console and CLI (command line interface) in an IDE
- IDE includes a console for user input and program output. 
- A #console or #terminal is a text-based interface that allows a user to run programs, enter input and view program output
- A consoles command-line interface #CLI isa an interface that allows the user to enter commands to run programs and work with files
- #commandLineArguments (think of something like a flag when doing things in bash) cp -r
## Why whitespace and precision matter
- #whitespace  is any blank space or newline
- Most coding activities require a student program's output to match exactly the expected output, including whitespace.
- Whitespace will impact the output of a program
-
### Programming is all about precision
- Programs mus be created precisely to run correctly
	- EX:
		- = and == have different meanings
		- Using i where j was meant can yield a hard to find bug
		- Not considering that n could be 0 in a sum/n 
		- Counting from i being 0 to i < 10 vs i <= 10
### Other random
- #incrementalDevelopment is a valuable programming practice where code is written, compiled and tested in small chunks with each step involving a small increment of additional code.
- This helps manage complexity and identify issues early
- 
# Review Questions
- What does a print statement do?
- What is an IDE?
- What is a CLI?
- What are the type of error messages that can pop up?
- How do you convert input types?
- What is an algorithm
- What is computational thinking?
- What is whitespace and why does it matter?