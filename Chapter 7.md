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