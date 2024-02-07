# Chapter 3 - Functions

- A major purpose of functions is to group code that gets executed multiple
times. Without a function defined, you would have to copy and paste

## Parameter 
- Is a variable that an argument is stored in when a
function is called.

## Argument 
- It is the value that we pass to the function

## Return
- In general, the value that a function call evaluates to is called the
return value of the function.

## None Value
- It represents the absence of a value.
- Must be typed with a capital ``N``
- ``None``
- Python adds return None to the end of any function definition with no return statement. This is similar to how a while or for loop implicitly ends with a continue statement. Also, if you use a return statement without a value (that is, just the return keyword by itself), then ``None`` is returned.

## Keyword Arguments and ``print()``
- Most arguments are identified by their position in the function call.
- Keyword arguments are identified by the keyword put before them in the function call.
- Keyword arguments are often used for ***optional parameters***.

## Local and Global Scope
- **Local Scope** - parameters and variables that are assigned in a called function.

- **Gloabl Scope** - variables that are assigned outside all functions.

- **Scope** - container for variables.

- **Note 1**: it is a bad habit to rely on global variables as your programs get larger and complex.

- **Note 2**: If you ever want to modify the value stored in a global variable from in a function, you must use a global statement on that variable.

- **Note 3**: Writing functions without global variables is encouraged.


## 4 rules to tell whether a variable is in a Local or Global Scope

1. If a variable is being used in the global scope (that is, outside of all
functions), then it is always a global variable.
2. If there is a global statement for that variable in a function, it is a global
variable.
3. Otherwise, if the variable is used in an assignment statement in the
function, it is a local variable.
4. But if the variable is not used in an assignment statement, it is a global
variable.

## Exception Handling
- You want the program to detect errors, handle them, and then continue to run.

## Summary:
- Functions are a great tool to help you organize your code. You can think of
them as black boxes: they have inputs in the form of parameters and outputs in
the form of return values, and the code in them doesn’t affect variables in other
functions.
- ``try`` and ``expect`` statements can run code when an error has been detected.