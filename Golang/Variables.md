# Variables

### What is a variable?
Variable is the name given to a memory location to store a value of a specific type. There are various syntaxes to declare variables in Go. Let’s look at them one by one.

### Naming Conventions
- A variable name can only start with a letter or an underscore.
- It can be followed by any number of letters, numbers or underscores after that
- Go is case sensitive so uppercase and lowercase letters are treated differently.
- The variable name cannot be any keyword name in Go
- There is no limit on the length of the variable name.
- But it is advisable to have the variable name of optimum length.

## Declaring a variable

In GO variables are declared using the var keyword but there are other ways of declaring a variable too as we will see later in this tutorial. Let’s explore different ways of declaring a variable

### Declaring a single variable

`var name type` is the syntax to declare a single variable.

```
package main

import "fmt"

func main() {
	var age int // variable declaration
	fmt.Println("My age is", age)
	age = 29 //assignment
	fmt.Println("My age is", age)
	age = 54 //assignment
	fmt.Println("My new age is", age)
}
```
The statement `var age int` declares a variable named age of type int. We have not assigned any value to this variable. If a variable is not assigned any value, Go automatically initializes it with the zero value of the variable’s type.
The above program will print the following output.
```
My age is  0
My age is 29
My new age is 54
```
### Declaring a variable with an initial value
A variable can also be provided an initial value when it is declared. The following is the syntax to declare a variable with an initial value.
```
var name type = initialvalue

```
If a variable has an initial value, Go will automatically be able to infer the type of that variable using that initial value. Hence if a variable has an initial value, the type in the variable declaration can be removed.
```
var name = initialvalue

```
### Multiple variable declaration

Multiple variables can be declared using a single statement.`var name1, name2 type = initialvalue1, initialvalue2` is the syntax for multiple variable declaration.
The **type** can be removed if the variables have an initial value.
There might be cases where we would want to declare variables belonging to different types in a single statement. The syntax for doing that is
```
var (
      name1 = initialvalue1
      name2 = initialvalue2
)
```
### Short hand declaration
Go also provides another concise way to declare variables. This is known as short hand declaration and it uses `:=` operator.
**This syntax is only available inside functions.**
`name := initialvalue` is the short hand syntax to declare a variable.It is also possible to declare multiple variables in a single line using short hand syntax.
**Short hand declaration requires initial values for all variables on the left-hand side of the assignment**
Short hand syntax can only be used when at least one of the variables on the left side of := is newly declared.
```
package main

import "fmt"

func main() {
	a, b := 20, 30 // declare variables a and b
	fmt.Println("a is", a, "b is", b)
	b, c := 40, 50 // b is already declared but c is new
	fmt.Println("b is", b, "c is", c)
	b, c = 80, 90 // assign new values to already declared variables b and c
	fmt.Println("changed b is", b, "c is", c)
}
```
Whereas if we run the program below,
```
package main

import "fmt"

func main() {
	a, b := 20, 30 //a and b declared
	fmt.Println("a is", a, "b is", b)
	a, b := 40, 50 //error, no new variables
}
```
it will print error `/prog.go:8:10: no new variables on left side of :=` This is because both the variables **a** and **b** have already been declared and there are no new variables in the left side of **:=** in line no. 8
Since Go is strongly typed, variables declared as belonging to one type cannot be assigned a value of another type.

## Scope of a Variable (Local and Global Variable)

A variable declaration can be done at the package level or a function level or a block level. Scope of a variable defines where that variable is accessible and also the life of the variable. Golang variables can be divided into two categories based on scope

- Local Variable
- Global Variable

### Local Variable

- Local variables are variables which are defined within a block or a function level
- An example of the block is a for loop or a range loop etc.
- These variables are only be accessed from within their block or function
- These variables only live till the end of the block or a function in which they are declared. After that, they are Garbage Collected.

### Global Variable

- A variable will be global within a package if it is declared at the top of a file outside the scope of any function or block.
- If this variable name starts with a **lowercase** letter then it can be accessed from **within** the the package which contains this variable definition.
- If the variable name stats with a **uppercase** letter then it can be accessed from **outside** different package other than which it is declared.
- Global variable are available throughout the lifetime of a program

