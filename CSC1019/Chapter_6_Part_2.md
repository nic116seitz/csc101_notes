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
- #conditional_expression has the following form 
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