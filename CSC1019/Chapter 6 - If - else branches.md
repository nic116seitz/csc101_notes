# General
### Branch concept 
- Think putting different sized different groups of people at different sized tables
### Branch basics (if)
- #branch is a sequence of statements executed under a certain condition 
- if branch is a branch taken only if an expression is true
### If-else branches
- and if-else branch has two branches the first branch is executed if an expression is true, else the other branch is executed
### IF - elseif-else branches
- An if-else can be extended to an if -elseif-else sturcture
- Each branch condition is checked as soon as one of the branch's expressions is found to be true the branch is taken
- Of no expression is found true, execution will reach the else branch which then executes

# Chapter 6 questions
#reviewQuestions 
- What is a branch?
- what is an if branch?
- What makes an if else branch?

## Detecting equal values with branches
**Detecting if two items are equal using an if statement**
- A program commonly needs to determine if two items are equal
	- Ex: if a hotel gives a discount for guests on their 50th wedding anniversary, a program to calculate the discount can check if a variable num_years is equal to the value 50
- If statements execute a group of statements if an expression is true. The statements in a branch must be indented typically four spaces.
### Equality and inequality operators
- Whereas the equality operator checks whether two values are equal the inequality operator(!=) evaluates to true if the left and right sides aren't equal or different
- An expression involving an equality or inequality operator evaluates to a Boolean value (true or false)

| Equality operators | Description                      | Example (assume x is 3)             |
| ------------------ | -------------------------------- | ----------------------------------- |
| ==                 | a == b means a is equal to b.    | x == 3 is True  <br>x == 4 is False |
| !=                 | a != b means a is not equal to b | x != 3 is False  <br>x != 4 is True |
## If-else statement
- executes one group of statements when an expression is true, and another group of statements is false. 

### Multi- branch if-else statements
- this is for detecting multiple specific values of a variable an if-else statement can be extended to have three or more branches
- Additional branches use the #elif keyword which means else if
- Each branch's expression is checked in sequence
	- As soon as a evaluation statement is found to be true the branch executes
	- If no branch is found to be true than the else statement executes
# Detecting ranges with branches (general)
**Detecting ranges using if-elseif-else**
- This is a common programming task to detect numbers in a range and do something based on whether or not they fall in said range
- the lower range part is implicit from the previous expression being false 
### Using multi-branch if-else to detect ranges
- the sequential nature of multi-branch if-else statements is useful to detecting ranges of numbers
### Relational operators
- #relational_operator checks how one operand's value relates to another, such as being greater than 
- some operators such as >= involve two characters
	- (The combination of the two characters is non arbitrary)

| Relational operators | Description                                  | Example (assume x is 3)                                 |
| -------------------- | -------------------------------------------- | ------------------------------------------------------- |
| <                    | a < b means a is less than b.                | x < 4 is True  <br>x < 3 is False                       |
| >                    | a > b means a is greater than b.             | x > 2 is True  <br>x > 3 is False                       |
| <=                   | a <= b means a is less than or equal to b.   | x <= 4 is True  <br>x <= 3 is True  <br>x <= 2 is False |
| >=                   | a >= b means a is greater than or equal to b | x >= 2 is True  <br>x >= 3 is True  <br>x >= 4 is False |
- for relational operators when creating a equal to or less than or a greater than or equal to the non equal value always precedes the equal 
	- EX: 
		- Correct : `<=` or `>=`
		- Incorrect: `=>` or `=<`

### Detecting ranges with if-else statements
- Second branch is only reached if the first branch is false
### Operator chaining
- #operator_chaining 
	- ex: `a < b < c` 
		- This determines whether b is greater- than a but less-than c 
		- Chaining comparisons are left => right
		- If the first statement is evaluated as true then the next statement gets evaluated

### Logical **AND, OR** and **NOT** (general)
- #logical_operator : treats operands as being True or False and evaluates to T or F
- #Boolean : refers to a value that is either T or F

## Logical operators table

| Logical operator | Description                                                                                     |
| ---------------- | ----------------------------------------------------------------------------------------------- |
| a **and** b      | Boolean AND: True when both operands are True.                                                  |
| a **or** b       | Boolean OR: True when at least one operand is True.                                             |
| **not** a        | Boolean NOT (opposite): True when the single operand is False (and False when operand is True). |

## Examples of logical operators

`Given age = 19, days = 7, user_char = "q"`

|                              |                                                                 |
| ---------------------------- | --------------------------------------------------------------- |
| `(age > 16) and (age < 25)`  | True, because both operands are True.                           |
| `(age > 16) and (days > 10)` | False, because both operands are not True (days > 10 is False). |
| `(age > 16) or (days > 10)`  | True, because at least one operand is True (age > 16 is True).  |
| `not (days > 10)`            | True, because operand is False.                                 |
| `not (age > 16)`             | False, because operand is True.                                 |
| `not (user_char == "q")`     | False, because operand is True.                                 |
## Detecting ranges with gaps
### **Basic ranges with gaps**
- Ranges contain gaps
	- EX: people who qualify for a discounted movie ticket on the basis of being an elder or a child 
- else if statements can be used to detect these gaps
- Logical operators are used to explicitly detect ranges with an upper and lower bound



## **Multiple distinct if statements**

- Sometimes the programmer has multiple if statements in seq., which looks similar to a multi-branch if statement

- However it has a different meaning

- Each if statement is independent and more than one branch can execute

## Nested if-else statements

- If else statement inside of an if-else statement

## Comparing data types and common errors

**Comparing int, str, and float types

- The relational and equality operators work for int, string and float

- float should not be compared using equality operators

- equal for str follows strict == (think js)

- type of comparison is determined by the things being compared

- If you compare things that make no sense you will get a type error (1 > squid)

  

### Notes on comparison

- nums are arithmetically compared 

- strs are compd by converting each char into a num value

    - most strings comparison use equality operators == or !=

- Lists and tuples are compared via an ordered comparison of every element in the sequence

    - Relational ops can also be used

    - Result is determined by the first mismatching elements in the seq

- Dicts are only compared with == != to be equal the 2 dicts must have the same set of keys and corresponding value for each key

  

## Common branching errors

- using = vs == 

  

# Order of evaluation

**Precedence rules**

| Operator/Convention       | Description                                                              | Explanation                                                                                                                 |
| ------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| ( )                       | Items within parentheses are evaluated first                             | In `(a * (b + c)) - d`, the + is evaluated first, then *, then -.                                                           |
| * / % + -                 | Arithmetic operators (using their precedence rules; see earlier section) | `z - 45 * y < 53` evaluates * first, then -, then <.                                                                        |
| <   <=   >   >=   ==   != | Relational, (in)equality, and membership operators                       | `x < 2 or x >= 10` is evaluated as `(x < 2) or (x >= 10)` because < and >= have precedence over or.                         |
| not                       | not (logical NOT)                                                        | `not x or y` is evaluated as `(not x) or y`.                                                                                |
| and                       | Logical AND                                                              | `x == 5 or y == 10 and z != 10` is evaluated as `(x == 5) or ((y == 10) and (z != 10))` because and has precedence over or. |
| or                        | Logical OR                                                               | `x == 7 or x < 2` is evaluated as `(x == 7) or (x < 2)` because < and == have precedence over or.                           |
**Common error: Missing ()**

- This causes the expression to be evaluated in a different order than expected

- Good () use makes the order of operations explicit

## Code blocks and indentation 

#### Code Blocks

- #code_block is a series of statements grouped together. 

- Code block is defined by its indentation lvl

- Initial code block not indented

- New code block can follow a statement that ends with a colon such as an "if" or "else"

- The amount of indentation is arbitrary as long as it is consistent

- ***Good practice is to use the standard recommended 4 columns per indentation level***

- A common error for newer python programmers is the mixing of tabs and spaces never mix tabs and spaces for indentation in the same program

### Special Cases

- The acceptable number of columns varies from 80 to 120. Good practice is to use the widely accepted standard of 80 columns

## Conditional expressions

#### Conditional expressions

- #conditional_expressino has the following form 

    - `expr_when_true if conditon else expr_when_false`

        - All three operands are expressions

        - Condition in the middle is evaluated first

        - If the condition evaluates to true then expr_when_false is evaluated

- conditional expression has three operands and thus sometimes referred to as a #ternary_operation 

- ***Good practice is to restrict the usage of conditional expressions to assignment statements***

- Some python programmers denounce conditional expressions as difficult to read

  

# Reading from Python [docs](https://docs.python.org/3/tutorial/controlflow.html)

### if Statements

- else is optional

- 0 <= elif parts 

- #match_statement may also be useful [link]()

#### for Statements

- differs in py a bit compared to how it is used in C or Pascal

- py's for statement iterates over the items of any sequence in the order that they appear in the sequence

- Ex:

  

```

>>># Measure some strings:

>>>words = ['cat', 'window', 'defenestrate']

>>>for w in words:

       print(w, len(w))

cat 3

window 6 

defenestrate 12

```

  

## the range() Function

- good for iterating over a sequence of numbers 

- end point is never part of the sequence