### VARIABLE AND PRINT COMMAND

#### Variable

A variable is used to hold a value or command, in GOLANG - a variable are assigned a type either explicitly or implicitly

Below is a syntax of declaring a variable
```
var <variableName> <dataType> = <value>
var     name         string   =   "Joe"
```
A variable can also be declared using the `shorthand` method as below
```
name := "Joe
```
#### Variable Scope - Local & Global
A local variable is declared inside a function or block and it's not accessible outside of that function or block.

A global variable is declared at the top of all function or block and it's available throughout the lifetime of the programme, it can also be accessed from any part of the programme.

Example of local and global scope variable

```go
// Local Variable
package main
import ("fmt")

func main() {
  name := "Joe"
  fmt.Println(name)
}
```

```go
// Global Variable
package main
import ("fmt")

var name string = "Joe"
func main() { 
  fmt.Println(name)
}
```

#### Printing Variable
In GOLANG, the `fmt` can be used to print out the values in a variable.

The following are some of the various methods of printing available in the `fmt` package.

* `fmt.Print`: used to print output to a line
* `fmt.Println`: used to print output to a new line
* `fmt.Printf`: used for formatting print output

Printf format specifiers
```
Verb    Description

%v  ->  default format
%T  ->  type of the value
%d  ->  integers
%c  ->  character
%q  ->  quoted characters/string
%s  ->  plain string
%t  ->  true or false
%f  ->  floating numbers
%.2f  ->  floating numbers upto 2 decimal places
```

#### User Input
The `fmt` package also has a method used to read input from the user, this is referred to as the `fmt.Scanf`. This method is used to read input from the standard input(usually from a console) and store it in a variable. It takes in two main argument (format string & a variable). The format string specifies the type of expected input while the variable is used to hold or store the input values.

Example
```go
package main
import "fmt"

func main() {
var name string
fmt.Print("Enter your name: ")
fmt.Scanf("%s", &name)
fmt.Println("Hey there, ", name)

// Running the programme and enter a name in the console
>>> go run main.go
Enter your name: Joe
Hey there, Joe
}
```

Also, the `fmt.Scanf` also return the following outputs
* count: shows the number of arguments that the function writes to
* err: display any error thrown during the execution of the function