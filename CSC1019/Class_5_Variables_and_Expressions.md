## Variable Assignment
- #variable is a named item that holds a value
- #assignmentstatement assigns a variable with a value such as x = 5
	- x = 5 until it is re assigned
- = does not mean equals it means assignment
## Assignments with variable on left and right
- basic review on incrementing
- x = x + 1 
- use += 1
- An assignments left side must be a variable
## Rules for identifiers
- #identifier = name
	- is a sequence of letters  underscores and digits 
	- must start with letter or underscore
	- names can start with double underscore but should be avoided as python has special use for this 
	- names are case sensitive 
	- and or true can't be used #reserved_words or #keywords
## Style guidelines for identifiers
- good practice for py is to use all lowercase underscore separated words 
- PEP 8 is the style guide
- keep names short
## Reserved words
| False  | Await    | else    | import   | pass       |
| ------ | -------- | ------- | -------- | ---------- |
| None   | break    | except  | in       | raise      |
| True   | class    | finally | is       | return<br> |
| and    | continue | for     | lambda   | while      |
| as     | def      | from    | nonlocal | with       |
| assert | del      | global  | not      | try        |
| async  | elif     | if      | or       | yield      |
## Objects
- #object represents a value and is automatically created by the interpreter when executing lines of code
- objects are discarded from mem after printing
- deleting objects automatically is #garbage_collection
## Name binding
- #name_binding is the process of associating names with interpreter objects
- object can have more than one name
- every name is bound to one object
- #name_binding occurs when assignment statement is executed
## Object properties
- #value : such as "20" or "string"
- #type : the type of object // int, str, bool
- #identity : unique identifier that describes the object
- type determines supported behavior
	- Ex: ints can be added
	- strings can be appended
- type() returns object type
- type also determines mutability
- #mutability indicates whether the object's value can be changed
- ints and str are immutable
- changing the value through reassignment creates a new object and names being bound to said new object
- #identity is the unique numeric identifier 
- only one object can hold a particular identifier
- identity refers to the memory address where the object is stored
- to find this use the built in function  ` id() `

## Numeric Types Floating- Point
- #float is a real number like 98.6
- floating point refers to the decimal point appearing anywhere in the number
- Is the data type for floating-point numbers
- #floating_point_literal written with the fraction part 
	- Ex: 10.0
#### Scientific notation
- useful for representing floats much greater or less than 0
#### Overflow
- floats have limited range of values that can be expressed
- For standard 32bit  python max is 1.8e308 min is 2.3e-308
- Overflow occurs when a value is too large to be stored in mem allocated by interpreter
#### Manipulating float output
- syntax for outputting a float with 2 digits after the decimal point:
	- `print(f"{my_float:.2f}")`
	- you can  adjust the number in front of the last f to alter how many digits are shown after the point
	- When you reduce a number in this way this has a rounding effect
## Arithmetic expressions
### Basics
- #expression = combination of items that evaluate to a value
	- variables, literals, operators, and parentheses
- #literal = specific value in code like 2
- #operator = that performs a built-in calculation 
- expressions don't include the equal sign 
### Evaluation of expressions
- expressions evaluate to a value which replaces the expression 
### Python expressions
- A good practice is to include a single space around operators for good readability (excluding -negate )
### Compound operators
- these are a shorthand for updating a variable
- += , -=, \*=,  /=, %=

- You cannot use commas in an integer literal

## Division and modulo
### Division integer rounding
- division operator  performs division and returns a floating point number
- // = floor division which rounds down the result of floating point division to the closest smaller whole number value
### Modulo examples
```
ones_digit     = user_val % 10    # Ex: 927 % 10 is 7. 
tmp_val        = user_val // 10   # 

tens_digit     = tmp_val % 10     # Ex: tmp_val = 927 // 10 is 92. Then 92 % 10 is 2.
tmp_val        = tmp_val // 10

hundreds_digit = tmp_val % 10     # Ex: tmp_val = 92 // 10 = 9. Then 9 % 10 is 9.
```
- A expression that uses module can only evaluate from 0 to n-1 
	- Ex: n % 6 < 6 
- If you wanted to target the number in the middle of a 3 digit number what you would have to do is the following
```
x = 693
(x // 10) % 10
```
- in the above example you are using the // function to remove the 3 because 693 / 10 resolves to a number that rounds to 69 (this removes the right most digit)
- then you modulo the 69 by 10 as 10 only fits evenly into 60

## The math Module
- this is for supporting advanced math operations
- Modules are located in another file
- sqrt() is an example that takes a number and calculates the square root
- #function_call is the process of invoking a function
- the item passed to a function is referred to as an argument
Commonly used functions:
#function_list
**Number representation and theoretic functions**

| Function     | Description                               |
| ------------ | ----------------------------------------- |
| ceil(x)      | round up value                            |
| factorial(x) | factorial ex: (3! = 3 \* 2 \* 1)          |
| fmod(x, y)   | remainder of division                     |
| fabs(x)      | absolute value                            |
| floor(x)     | round-down value                          |
| fsum(x)      | floating point sum of range list or array |
**Power Exponential and logarithmic functions**

| Function       | Description                         |
| -------------- | ----------------------------------- |
| exp(x)         | Exponential function e^x            |
| pow(x, y)      | raise x to the power of y           |
| log(x, (base)) | natural logarithm; base is optional |
| sqrt(x)        | square root                         |
**Trigonometric functions**

| Function                   | Description                     |
| -------------------------- | ------------------------------- |
| acos(x)                    | Arc cosine                      |
| atan(x)                    | Arc tangent                     |
| cos(x)                     | Cosine                          |
| hypot(x1, x2, x3, ..., xn) | Length of vector from origin    |
| radians(x)                 | Convert degrees to radians      |
| cosh(x)                    | Hyperbolic cosine               |
| asin(x)                    | Arc sine                        |
| atan2(y, x)                | Arc tangent with two parameters |
| sin(x)                     | Sine                            |
| degrees(x)                 | Convert from radians to degrees |
| tan(x)                     | Tangent                         |
| sinh(x)                    | Hyperbolic sine                 |
**Complex number functions**

| Function | Description    |
| -------- | -------------- |
| gamma(x) | Gamma function |
| erf(x)   | Error function |
**Mathematical constants**

| Function     | Description                       |
| ------------ | --------------------------------- |
| pi(constant) | mathematical constant<br>3.141592 |
| e(constant)  | Mathematical constant<br>2.718281 |
## Random numbers
**Generating random numbers**
- #random  module provides methods that return random values
- random() returns a random floating-point value each time the function is called
- In order to use random you need to put `import random` at the top of your .py
- Numbers will be 0(inclusive) to 1 (exclusive)
	- This means that it will return a number up to the number you have selected not including the number written
- you can create a range of number generations using the following two functions
- `randint(min, max)` 
	- This will produce a random int between min and max inclusive
- `randrange(min, max)`
	- This will produce a random int between min and max - 1 inclusive
- For this 0 is counted as one of the numbers (meaning that if the number at the bottom of the range is less than 0 the range that will be produced will be the absolute value of the range)
	- Ex:` random.randrange(-x,0) // This produces x values as the |-x| = x ` 
**Pseudo-random**
- the numbers generated by the random module are pseudo random (not really just appearing to be random)
- There is an underlying equation to compute the next random number
- Intial number is based on current time (this is called a seed)
- You can force a seed number using `random.seed(x)` 
	- This is useful for testing reasons
## Representing text
**Escape sequences**
- newline is an example
- escape sequences start with \

| Escape Sequence | Explanation      | Example code                                  | Output                                   |
| --------------- | ---------------- | --------------------------------------------- | ---------------------------------------- |
| \\\             | Backslash (\\)   | print("\\home\\users\\")                      | \home\users\|                            |
| \\'             | Single quote (') | print('Name: John O\'Donald')                 | Name: John O'Donald                      |
| \\"             | Double quote (") | print("He said, \"Hello friend!\"")           | He said, "Hello friend!"                 |
| \n              | Newline          | print("My name...\nIs John...")               | My name...<br>Is John...                 |
| \t              | Tab (indent)     | print("1. Bake cookies\n\t1.1. Preheat oven") | 1. Bake cookies<br>    1.1. Preheat oven |
**Raw strings and converting between an encoding and text**
- Esc sequences can be ignored using raw string
- this is done by pre-pending a string literal with r
- ord() returns an encoded value for a string length one
- chr() returns string of one character for an encoded int

## Style guidelines
- these change according to team, oss project or classroom
- This is to create consistency across a team 

**Whitespace**
[This is the link to the class style](https://learn.zybooks.com/zybook/RRCCCSC1019McAfeeFall2025/chapter/5/section/11)

# Review Question
#review_Questions
- What are the reserved words?
- What does ord()
- What does chr() do?
- How does the random Module Work?
- What are escape sequences?
	- How do they work?
- What does sqrt() do?
- What is Modulo?
- What is randint?
- What is randrange?