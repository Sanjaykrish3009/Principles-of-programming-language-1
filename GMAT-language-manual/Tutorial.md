## ***TUTORIAL***


### Introduction

GMAT program is used to solve general problems with a special purpose of solving 2d geometry problems and also plot the graph and which can also be extended to 3d geometry and complex solving. GMAT only includes the libraries which are required to our code and also the libraries in GMAT support object oriented programming.

This write up gives the glimpse of variables, arrays, functions, Arithmetic expressions,loops, arguments and scope.

### 1.1 First program

To build our programming language the common needs for it are variables, header files, libraries, main function, indentation, functions, etc. Let’s get started with our first program, which is generally the first-ever program written in any other programming language.
Printing the words
Hello, world
```js
add_lib :+ io.LIB
main::_num
    write(“hello world\n”)
    return 0
```
you must create the program in a file with its extension “  .gm'', such as hello.gm, then compile it. If you haven't messed up anything like omitting a character or misspelling something or defining the variables compilation would be successful, and an executable file would be created.
Our programming language consists of functions, variables. Our language also includes libraries that are mentioned in the program as per our requirements. The first line of our program ie.,

                  add_lib :+ io.LIB
tells the compiler to include information about the standard input/output library. The second line main::_num is the main function of the program, where the program begins so every program must contain this line, _num is the return type argument in the main function. The main function calls all the required libraries and functions which are required for use in our program.

The third line write(“hello world\n”) which prints whatever is written inside the write() function and \n is a newline character, the next output will be printed in the next line. The write() function is an inbuilt function in io.LIB library. Line \n we have \t, \b for tab space and backspace.
The fourth line return 0 means if the main function executes without any errors then it returns the value 0.  The indentation of the program is an important characteristic of this language.


### 1.2 Variables and Arithmetic Expressions

This program uses the arithmetic expressions and depicts the importance of precedence order of the expressions i.e, the order of operations that tells which operations to be performed first in order to evaluate the given mathematical expression.
```js
add_library :+ io.LIB

main::

    ~~precedence order is the same as in all languages
    ~~ parsing is done from left to right

    _num x=0,y=0

    x = 3+4*5/2*8%2
    y = 3+4/2*5+8%3
    write(x," ",y)

return 0
~~ _num allocates memory according to the value assigned to the variable
```
The “precedence order is the same as in all languages” line of the program is a comment, an act of adding notes which is programmer readable. Any instruction after ```“~~”``` in that line will be ignored by the compiler i.e, a single line comment, and any instructions between ```“~”``` and ```“~”``` will also be ignored by the compiler i.e, maybe a multi-line comment.

We have declared variables in the “_num x=0,y=0” line of the program._num allocates the memory according to the value assigned to the variable. Declaration of variables consists of type and variable names and maybe their initializations sometimes. Here the type is _num that means the variables consist of numbers and variable names are x & y which each is initialized to the value 0. The variable names can contain letters, digits, and start with an alphabet. And Gmat is case sensitive. While naming the variables, keywords should not be used as variable names.


The lines “x = 3+4*5/2*8%2” & “y = 3+4/2*5+8%3” gives the mathematical expressions to be evaluated. And these two expressions show us the importance of precedence order. The first mathematical expression i.e, 3+4*5/2*8%2 will be evaluated in the following order
```
3+4* 5/2*8%2
3+20/2*8%2
3+10*8%2
3+80%2
3+0
3.
```
And the second mathematical expression i.e, 3+4/2*5+8%3 will be evaluated as
```
3+4/2*5+8%3
3+2*5+2
3+10+2
13+2
15
 ```
And here you can see that these two expressions give two different answers, and this tells the importance of the precedence order. The precedence order of the arithmetic operators is
        +,- have same precedence
*,/,% have the same precedence
precedence(*,/,%) > precedence(+,-)

    The line “write(x," ",y)” prints the value of x & y with a space between them as given by the programmer.



### 1.3  The for statement

Program to print the sum of the given first n number of natural numbers
```js
add_lib :+ io.LIB
main::_num
    _num count,sum=0, n
    write(“Enter a positive integer : “)
    read(n)
    ~~ for loop terminates when number is less than count
    for:count = 1,count<=n: count++
        sum++count
    write(“Sum = ”,sum)
    return 0
```
We defined three variables named as count, sum,n of data type _num, with the sum being initialized to 0. In the second line, we have to give the input value for the number. In the third step, it is for a loop. The for statement is a loop, a generalization of the while, there are three parts. The first part is initialization

                             count = 1
The second part is the condition that controls the loop
                         count <= n
If the above condition return true then the body of the loop is executed (here it is sum = sum+count)
 Then the increment step

                      count = count ++   ie., count = count+1
The loop gets executed till the condition returns false, then the loop terminates and the statement out of the for loop will be executed here it writes the final value of the sum.

The choice between while and for is arbitrary. All for loops can be written as while loops, and vice-versa. Just use whichever loop seems more appropriate to the task at hand. In general, if you are aware of the number of times of execution of the loop beforehand, using for loop would be better. If you want the loop to break based on a condition other than the number of times it runs, you should use a while loop.


### 1.4 Symbolic Constants

The programmer can define quantities that convey information to someone who is reading the program later on and these are hard to change in a systematic way. One way to deal with these quantities is to give them some meaningful names using the conventions of naming a variable. We use the term #define to do this.

For example

```    #define name quantity```

Hereafter any occurrence of “name” will be replaced by the corresponding quantity. There are no limitations for the quantity, it can be anything.
```js
add_lib :+ io.LIB
#define PI 3.14159
Main::_num
    _num r
    write(“Give radius of the circle:”)
    read(r)
    write(“Area of the circle is “,PI*r*r,”.”)
return 0
```
Here the quantity PI is symbolic constant which gives the value of constant ]\

### 1.5 Input and Output
Input means to feed some data into a program. An input can be given in the form of a command line or file. Output, it means to display data on screen or in a file. GMAT programming provides a set of built-in functions to execute these commands.
#### 1.5.1) Getchar and putchar
 The _num getchar(void) function reads the next available character from the screen and returns it as an integer. This function reads only a single character at a time. We have to write a loop for printing more than one character.


The _num putchar(_num c) function puts the passed character on the screen and returns the same character. This function puts only a single character at a time. We have to write a loop for printing more than one character.
```js
add_library:+ io.LIB
main::_num
_num c
c = getchar()
     while:c != EOF
        putchar(c)
        c = getchar(c)
When getchar is inside the loop the equivalent program is
add_library:+ io.LIB
main::_num
_num c
     while:(c = getchar()) != EOF
putchar(c)
        c = getchar(c)
The precedence value of != is greater than =, so we need to add a parentheses, in absence of parentheses c= getchar() != EOF is equivalent to c = (getchar() != EOF)
```

#### 1.5.2 word counting
```js
~~ count lines, words, and characters in input

add_library :+ io.LIB
main::_num
_num c, nl=0, nw=0, nc=0, state, INSIDE =1, OUTSIDE = 0
state = OUTSIDE
while: (c = getchar()) != EOF
     nc++1
if : c == '\n'
nl++1
if : c == ' ' || c == '\n' || c == '\t'
state = OUTSIDE
else if : state == OUTSIDE
state = INSIDE
nw++1
write( nl, nw, nc)
```
If else statements are used to count lines and words. A while is used to repeat the loop, EOF character is the end of file where the while loop terminates. And this operator || means OR, if c is any one of these black space, new line or a tab space  then the if statement executes.

### 1.6 Arrays

An array is a collection of variables stored at contiguous memory locations. This makes it easier to calculate the position of each element by adding the offset to the base value. The lowest address corresponds to the first element and the highest address to the last element.
This is an example of sorting an array. First, it reads the max number of elements in the array read(n), declaration of an array  _num Array[n] the elements of the array Array[0], Array[1],..........Array[n-1].


```js
add_library :+ io.LIB

main::_num
    _num n
     write("Enter the number of elements of array:")

    _num Array[n]
    write("Enter the elements of array:")

    for:_num(i=0),i++:i<n:
        read(Array[i])

    for:_num(i=0), i++:i<n:
        for:_num(j=i+1), j++: j<n:
            if:Array[i] > Array[j]
                _num temp = Array[i]
                Array[i] = Array[j]
                Array[j] = temp

    write("Sorted array:")

    for:_num(i=0),i++:i<n:
        write(Array[i]," ")            

    return 0
```

  In this code, the datatype of the Array is _num. The for loop in the array to read the elements of the array. The next two for loops and if loop is to sort the array elements in ascending order and at last for loop to print the array in sorted order.


### 1.7 Functions

A function is a block of organized, reusable code that is used to perform a single related action. Functions provide better modularity for our application and a high degree of code reusing. Till now we have seen functions like read(), write(), main() which are inbuilt functions provided by the language itself. In GMAT, a function can return more than one value.
The syntax of the function in GMAT is -
Function_name: arguments : return_types
Here in this program we are solving the roots of the equation.
 ```js
add_library :+ io.LIB
add_library :+ geo.LIB

func:_str expression, _num degree:void
    _poly Eq:degree
    Eq = [expression]
    _num x[degree]
    x = Solve[Eq]
    for:_num i=0,i<degree:i++
        write(x[i]," ")
    write("\n")

main::_num
    _num n
    write("Enter the degree of equation:")
    read(n>-1)

    _num expression[n+1]
    write("Enter the coefficients in order:")
    for:_num i=0,i<n+1;i++
        read(expression[i])
    func:expression,n:
    return 0    
```

First we are finding the degree of the equation, read(n>-1) means degree will ask the value until the user gives a value greater than -1, _num expression[n+1] is an array of coefficients and then  ``` func:expression,n: ```  we are calling this function to solve the roots. In the function the arguments are ``` _num expression[]``` , _num n and then we are defining the
```_poly Eq:degree```  where we are storing the expression in the equation with a degree n. Now we are using an inbuilt function

```x = Solve[Eq]``` to find the roots of the equation and using a for loop we are printing them.


### 1.8 Arguments- Call by value and call by reference
##### Call by reference :
The call by reference method copies the address of an argument into the formal parameter. In this method, the address is used to access the actual argument used in the function call. It means that changes made in the parameter alter the passing argument.


Program to swap two numbers :

```js
add_library :+ io.LIB
swap:_num *a, _num *b: void
    _num temp
    temp = *a
    *a = *b
    *b = temp
    write(“After swapping values in the function a = ”,a,”, b = ”, b)
main::_num
    _num a = 10, b = 20
    write(“Before swapping the the values in the main a = ”,a,”, b = ”,b)
    swap:&a,&b:
    write(“After swapping the the values in the main a = ”,a,”, b = ”,b)
    return 0
```
In the above example, The variables a,b are initialized with values 10, 20. In the second line, the initial values of a and b will be printed. In the third line of the main function, we call the function swap by passing addresses of the variables a and b as arguments. The address is used to access the actual argument passed in the function call. Therefore the changes we make in the parameter will alter the passing argument.

#### Call by value :
Arguments are passed “by value”, this means the value of the actual arguments is passed into the respective temporary arguments. Therefore, changes made to the parameter of the main function do not affect the argument.
```js
add_librabry :+ io.LIB
swap : _num a, _num b
     _num temp
     temp = a
     a = b
     b = temp
     write(“After swapping values in the function a = ”,a,”,b ”, b)

main::_num
    `_num a = 10, b = 20
    write(“Before swapping the the values in main a = ”,a,”, b = ”,b)
    swap(a,b);
    write(“After swapping the the values in th`e main a = ”,a,”, b = ”,b)
    return 0
```
In the above example, the values of the variables a and b are passed as arguments in the function call. The changes we make in parameters in the swap function will not alter the actual arguments.


Unlike call by reference, the changes made to the parameters in the function will not reflect in the actual arguments. In Call by value, actual and formal arguments will be created in different memory locations whereas in Call by reference, actual and formal arguments will be created in the same memory location.


### 1.9 Miscellaneous functions
```Mathematical functions ``` :  sinx,cosx,tanx...etc

```String functions``` : strcpy,strcmp,strcat..etc

```Geometric functions``` :

In the following, A,B are defined with _polygon datatype Following functions
 take _polygon as arguments


*area(A)* -returns the area of A perimeter(A) -returns perimeter of A

*numberofDiagonals(A)*-returns the number of diagonals in A

*numberofSides(A)* -returns number of sides in A

*typeofTriangle(A)* -prints the type of triangle if A is a triangle, else return

*center(A)* -returns coordinates of center of A

*orthocenter(A)* -returns coordinates of Orthocenter of A if A is triangle, else return

*circumradius(A)* -returns the Circumradius of A if A is triangle, else return

*circumcenter(A)* -returns coordinates Circumcenter of A if A is triangle, else return

*getPropeties(A)* -prints all the above properties basing on polygon type of 'A'

*check_Congruence(A, B)* -prints "TRUE" if congruent, else
"FALSE"

```Conic functions:```

In the following A, B are defined with _conic datatype Following functions take _conic as arguments.

*focii(A)*     - returns coordinates of focii of A

*eccentricity(A)* - returns eccentricity of A

*focalLengh(A)*    - returns focal length of A

*lenghofmajoraxis(A)* -returnsnlength of major axis of A

*latusrectum(A)* - returns length of latusrectum of A

*conicProperties(A)* - prints all above properties of A

*typeofconic(A)* - prints type of conic A is


```Polynomial functions``` :

In the following A is defined with _poly B is an array of roots of a polynomial

solve(A) -returns the roots of A

getequation(B) - prints the coefficients of polynomial whose roots are in array B

### 1.10 External Variables and Scope
The scope of a name is the part of the program within which the name can be used.

The variables whose scope is throughout the program are called external variables i.e, it can be used throughout the program.
```js
add_library :+ io.LIB
main::_num
    _num x
    read(x)
    _num y,i
    for:i=0,i<x:i++
        y+=i
        _num y = i+1
        write(y," ")   ~~Its first preference would be the local variable

    write("\n")    
    write(y," ",i)   
~~the "y"-variables here prints the value stored in the 'y' outside the for loop
    return 0
```
This program gives us clarity about scope. In this program, the first write statement prints the value of ‘y’ which is resulted in the for loop as the first preference would be the local variable, and the second write statement prints the value stored in the ‘y’ outside the for loop.

In the programs where there are other functions than main, the variables declared in a function are local to that function. For a variable to be used in multiple functions, there is a possibility to define variables that are external to all functions and these are called external variables.
