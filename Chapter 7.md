# Loops
### **Basics
-  #loop is a program that repeatedly executes the loop's statements (loop body)
- Each step is called an iteration
- Loops only continue repeating while the loop's expression is true
## **Intro to while loops
- #while_loop runs a block of code repeatedly as long as the while loop's condition is true
- #sentinel_value is a value that causes a loop to end
- #Infinite_loops are loops are loops that never stop running because the loop's condition is awlays True
```

sentinel = "quit"
command = ""

while command != sentinel:
    command = input("Type quit to exit: ")
```
### **Counting with a while loop
- Counting is a common task in programming often done using a loop 
- #loop_variable can be used for counting and updating during each iteration until loop condition is false
## **For loops**
- Common task is to access all of the elements in a container one by one
- For loop can iterate over other containers such as strings and dictionaries
- A for loop iterates over each character in the string
- `reversed()` is a handy function for loops that will iterate the last element first
# Membership and Identity Operators
## Membership operators: in/not in**
- One task is to find a specific value in a container such as a list or dictionary
- In and not in operators known as #membership_operators yield a bool if the left operand matches the value of an element in the right operand which is always a container
- #membership_operators can be used with sequence types
	- If the variable x is a list or tuple then a `in` x evaluates to `True` if there exists an index idx for which `a == x[idx]` is True 
- #membership_operators can be used to check whether a string is a substring or matching subset of characters of a larger string 
	- abc == substring of 123abcd
- Membership in a dict implies that a specific key exists in the dictionary
## **Identity operators is/ is not**
- This is to check if two variables are the same object
- #identity_operator #is is for checking if two operands are bound to a single object
- Inverse == is not
- #identity_operator compare identities vs values
	- This is usually the memory address of an object
- *Be mindful that == and identity operator "is" are not te same *
	- This has to do with how python pre-creates for a small amount of values in order to not have to continously create them
- *Good practice is to avoid using the identity operators is and is not, unless checking to see if two objects are identical*
# Counting using the range() function
## **The range() function
- #range_function `range()` is used to iterate over all elements of a container.
- This allows for the counting ins for loops
- Range() generates a sequence of integers between the starting int that is included in the range and an ending int that int that is not included in the range as well as a step function

 # While vs for loops

## **Correspondence**
- For loop combined with range() is generally preferred over while loops
	- *For loops are less likely to become stuck in an infinite loop*
##### General Rules
- Use a #for_loop when the number of iterations is computable before enter the loop
	- Counting down from x to 0 printing a string n times
- Use a #for_loop when accessing the elements of a container
	- adding 1 to every element in a list
	- printing the key of every entry in a dict
- Use a #while_loop when the number of iterations is not computable before entering the loop
# Nested loops
## **Nested loops**
- A #nested_loop is a loop that appears as part of the body of another loop
	- They are referred to corresponding to position 
	- i.e inner/ outer loop

# Developing programs incrementally
## **Incremental Programming**
- Breaking up a big project into smaller projects an making sure that they work as you go
- or creating a simpler version of the program and fleshing it out as you go
# Break and continue
## **Break statements**
- A #break statement in a loop causes the loop to exit immediately
- This is for making a loop that is simpler to understand
## **Continue statements
- cause an immediate jump to the while or for loop header statement
- This is for better readability
## **Loop else
- For while loops this allows you to create a parameter once if the loop expression is evaluated as false
	- EX:
	  ```
	  cars = 0
	  while cars > 0:
		  cars += 1 
	  else:
		  print("This is an invalid amount of cars")
		
	  ```
 In this figure the else statement would execute once as a result of cars being equal to zero
 - In the case of a #for_loop the else statement would execute once the loop is complete
 - The #loop_else construct executes the loop normally
 # Getting bot index and value when looping: enumerate()
## **The enumerate() function**
- This is fore current index position as well as corresponding element value when iterating
- For loop that iterates over a container obtains the value directly but must look up the index with a function call
- #enumerate `enumerate()` retrieves both the index and the corresponding element value at the same time
	- This creates more readable cleaner code 

 