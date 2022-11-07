# CONTENTS
```
1) Introduction
2) Tutorial
2.1) Data types and Variables
2.2) Arithmetic Operators
2.3) Control Flow
2.4) Symbolic Constants
2.5) Input and Output
2.6) Arrays
2.7) Functions
2.8) Call by reference and call by values
2.9) External Variables and Scope
3) Language manual
3.1) Lexical components
3.2) Variables and Arithmetic Expressions
3.3) The for statement
3.4) SYMBOLIC CONSTANTS
3.5) Input and Output
3.6) Arrays
3.7) FUNCTIONS
3.8) Arguments- Call by value and call by reference
3.9) EXTERNAL VARIABLES AND SCOPE
4) Language Evolution
5) Examples
6) CRITICS
7) CONCLUSIONS
8)APPENDIX
```
## 1) Introduction :

GMAT program is used to solve general problems with a special purpose of solving 2d geometry problems and also plot the graph and which can also be extended to 3d geometry and complex solving. GMAT only includes the libraries which are required to our code and also the libraries in GMAT support object oriented programming.

This write up gives the glimpse of variables, arrays, functions, Arithmetic expressions,loops, arguments and scope.The core of the manual consists of a series of chapters on various topics. The topics have been chosen by the complexity, importance and frequency of their use in programming.

 ## 2) Tutorial

 #### 2.1 Data types and Variables

 Each variable is associated with a particular data type. Each data type requires different amounts of memory and has some specific operations which can be performed over it.

 ***Datatypes in gmat :***

 Different datatypes are :
 ``` _num, _str, _poly, _polygon, _point ,_line ```

 _num is a data type that stores  an integer irrespective of their size
 _str is a data type that stores the text, collection of characters
 _polygon is a data type that is used to store polygons (Ex: triangle, circle, etc.)
 _poly is a data type that stores the coefficients of the polynomial
 _point is a data type that stores two integers (x,y) which is used in solving 2d geometry problems

 Variables in gmat :
 A variable is the name of the memory location. It is used to store data. Its value can be changed, and it can be reused many times. It is a way to represent memory location through a symbol so that it can be easily identified.
 The variable names can contain letters, digits, and start with an alphabet. gmat is a case sensitive language. While naming the variables, keywords should not be used as variable names.
 _num, _str, _polygon, _point are variables that should start only with a character for example x, a1, b1, etc and in _poly, the variable should be in the form Eq:2, where 2 is the degree of the equation.
 ##### 2.2 Arithmetic operators

 An arithmetic expression is composed of operators and operands. Operators act on operands to yield a result. Commonly used arithmetic operators are +, -, *, / and %.  

 The “~~precedence order is the same as in all languages”

 The expression follows the BODMAS rule in general. The increment and decrement operators in gmat are x++, x--, x++y, x--y



|    Increment/ Decrement |   Equivalent operation         |
|----------|:-------------:|
| x++     |  x = x + 1|
| x-- |    x = x - 1  |   
| x++y | x = x + y |  
| x--y |    x = x - y |

    +, - have same precedence

    *, /, % have same precedence

    precedence(*, /, %) > precedence(+, -)

 ##### 2.3 Control Flow

 gmat consists control flow statements, which gives us a possible way to change the path of the CPU through the program.

 gmat supports if-else statements, for loop, while loop, switch statements.
```js
 If-else statements:
 	if: expression_1
 		statements
 	else if: expression_2
 		statements
 else: expression_3
 		Statements

 For loop:
 	For: initialization, Increment/Decrement: condition:
 		Statements

 While loop:
 	while: expression
 		Statements

 Switch statements:
 	switch : expression
         	case : constant_1 : statements
                    break
 		case : constant_2 : statements
                    break
 		.
 		.
 		.
 		default : statements
``` 	

 ##### 2.4 Symbolic Constants

 The programmer can define quantities that convey information to someone who is reading the program later on and these are hard to change in a systematic way. One way to deal with these quantities is to give them some meaningful names using the conventions of naming a variable. We use the term #define to do this.
 ###### SYNTAX OF SYMBOLIC CONSTANTS IN GMAT:

 	#define name quantity

 Hereafter any occurrence of “name” will be replaced by the corresponding quantity. There are no limitations for the quantity, it can be anything

 Examples:
```  
  #define size 10
  #define TRUE 1
  #define MAX 50
```

##### 2.5 Input and Output

 Input and output is the way for the outside world to communicate with the information processing system. The data received by the system is called input and the data sent from the system is called output.

 Taking input in gmat:
 ```js
 		data_type variable
 		read(variable)
```
 The variable in which the given data to be stored should be declared before using it in the function read.

 Giving output in gmat:
 ```js
 	write(“Welcome to gmat”)
 	data_type variable
 	write(variable)
  ```
 The one which is written in the double quotes in a write function will be printed as it is and the one which is not in the double quotes prints the value stored in it and this variable should be declared before.


 ##### 2.6 Arrays

 An array is a collection of variables stored at contiguous memory locations. This makes it easier to calculate the position of each element by adding the offset to the base value. The lowest address corresponds to the first element and the highest address to the last element.
 If there are n elements ina array then, the elements of the array :         ```Array[0],Array[1],..........Array[n-1].```

 ###### Declaration of Array :

 Type arrayName[arraySize]

 There are single dimensional arrays and also multi dimensional arrays.
 This is called a single-dimensional array. The arraySize must be an integer constant greater than zero and type can be any valid gmat data type. For example, to declare a 5 element array called Arr of type _num, use this statement _num Arr[5]

 ##### 2.7 Functions
 A function is a block of organized, reusable code that is used to perform a single related action. Functions provide better modularity for our application and a high degree of code reusing. Till now we have seen functions like read(), write(), main() which are inbuilt functions provided by the language itself. In GMAT, a function can return more than one value.
 The syntax of the function in GMAT is -  

 S.No
 GMAT function aspects

  syntax
  ```js
   1
 Function Call
 function_name(arguments)
   2
 Function definition
 function_name:arguments:return_types
 function body
```
 Example:
```js
    Function definition:
          Multiply:_num a,_num b:void
                   write(“product is”,a*b,” “)
                   return
    Function call:
          Multiply(a,b)
```

 ##### 2.8 Call by reference and call by value

 ###### Call by reference :
 The call by reference method copies the address of an argument into the formal parameter. In this method, the address is used to access the actual argument used in the function call. It means that changes made in the parameter alter the passing argument.

 ###### Call by value :

 Arguments are passed “by value”, this means the value of the actual arguments is passed into the respective temporary arguments. Therefore, changes made to the parameter of the main function do not affect the argument.

 ##### 2.9 External Variables and Scope
 The scope of a name is the part of the program within which the name can be used.
 	The variables whose scope is throughout the program are called external variables i.e, it can be used throughout the program.



## 3) Language manual


#### 3.1 Lexical components
###### 3.1.1 key words
Keywords are reserved for language processing, and they cannot be used for identifier or other purposes

Keywords in gmat are : for, if, elseif, switch, do, return, break, continue,true, false, etc.

###### 3.1.2 Identifiers
An identifier is used to name a variable or function, it could be any combination of lowercase letters (a to z),higher case letters(A-Z), number (0-9) or underscore(_), except that the first letter must be a lowercase character (a to z). An identifier cannot be an exact match with one of the reserved keywords
###### 3.1.3 Seperators




 |    Separators |   Usage       |
 |----------|:-------------:|
 | Comma - ‘ , ’    | Separates arguments in a function argument list, also separates two elements in the same row in a matrix literal. |
 | Parenthesis - ‘ () ’ |    Used to modify operator precedence, and to wrap the argument list of a function call.  |   
 | Double colon ‘::’ | Used in the declaration of all functions |  
 |Colon - ‘ : ’ |     Used to modify operator precedence, and to wrap the argument list of a function call. |







###### 3.1.4 Precedence table



|    Operators|    Associativity        |
|----------|:-------------:|
|  @    | left to right  |
| () [] -> .  |  left to right  |   
| ! ~ ++ -- + - * (type)|  right to left|  
| sizeof |     |
|  * / %    | left to right |
| + -     |    left to right  |   
| << >> | |  
| < <= > >= |  left to right   |
|  ==  !=  | left to right |
| &| left to right |  
| ^ | left to right    |
| \ | left to right |
|  \\\ |  left to right   |   
|= += -= *= /= %= &= ^=  |right to left  |  
| \\=   <<=  >>=    |   left to right   |
|  ,  |  |

Note : \ means '|' and \\ means '||'
###### 3.1.5 Newlines, Whitespaces and tabs

Newlines ('\n'), whitespaces (' '), and tabs ('\t') are used to split lexical components. Using one or more or any combination of them will make no difference.





#### 3.2 Variables and Arithmetic Expressions

Datatypes in gmat:

Different datatypes are
_num, _str, _poly, _polygon, _point
```
_num is a data type that stores  an integer irrespective of their size
_str is a data type that stores the text, collection of characters
_polygon is a data type that is used to store polygons (Ex: triangle, circle, etc.)
_poly is a data type that stores the coefficients of the polynomial
_point is a data type that stores two integers (x,y) which is used in solving 2d geometry problems
```
Variables in gmat :

The variable names can contain letters, digits, and start with an alphabet. gmat is a case sensitive language. While naming the variables, keywords should not be used as variable names.

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

The “```~~```precedence order is the same as in all languages” line of the program is a comment, an act of adding notes which is programmer readable. Any instruction after “```~~```” in that line will be ignored by the compiler i.e, a single line comment, and any instructions between “~” and “```~```” will also be ignored by the compiler i.e, maybe a multi-line comment.

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
                                      15.
```
And here you can see that these two expressions give two different answers, and this tells the importance of the precedence order. The precedence order of the arithmetic operators is
```
		+,- have same precedence
*,/,% have the same precedence
precedence(*,/,%) > precedence(+,-)
 ```
The line “write(x," ",y)” prints the value of x & y with a space between them as given by the programmer.

#### 3.3 The for statement

Program to print the sum of the given first n number of natural numbers
```js
add_lib :+ io.LIB
main::_num
	_num count,sum=0, n
	write(“Enter a positive integer : “)
	read(n)
	~~ for loop terminates when number is less than count
	for:count = 1, count++: count<=n:
		sum++count
	write(“Sum = ”,sum)
	return 0
```
We defined three variables named as count, sum,n of data type _num, with the sum being initialized to 0. In the second line, we have to give the input value for the number. In the third step,it will scan the given input and the next line is for loop. The for loop,can be considered as the  generalization of the while loop and there will be three parts in a for statement. The first part is initialization

                       count = 1
The second part is increment or the decrement that should happen after the execution of the body of the loop.
And the third part is the condition that controls the loop

                         count <= n
If the condition return true then the body of the loop is executed (here it is sum = sum+count)
Then the increment step

                        count = count ++   
                      i.e, count = count+1
The loop gets executed till the condition returns false, then the loop terminates and the statement out of the for loop will be executed. Here it writes the final value of the sum.
The choice between while and for is arbitrary. All for loops can be written as while loops, and vice-versa. Just use whichever loop seems more appropriate to the task at hand. In general, if you are aware of the number of times of execution of the loop beforehand, using for loop would be better. If you want the loop to break based on a condition other than the number of times it runs, you should use a while loop.

#### 3.4 SYMBOLIC CONSTANTS

SYNTAX OF SYMBOLIC CONSTANT IN GMAT:

	#define name quantity

Quantity can be either a value or set of characters(text)

Name is the symbolic name

At each occurrence of the symbolic constant, it is substituted by its corresponding value or text after the compilation of the program.

```js
add_lib :+ io.LIB
#define PIE 3.14159
Main::_num
	_num r
	write(“Give radius of the circle:”)
	read(r)
	write(“Area of the circle is “,PIE*r*r,”.”)
  return 0
```
Here the quantity PIE is symbolic constant which gives the value of constant
Here in this program we are solving the roots of the equation.

#### 3.5 Input and Output

Input means to feed some data into a program. An input can be given in the form of a command line or file. Output, it means to display data, may be on the screen or in a file. GMAT programming provides a set of built-in functions to execute these commands.
###### 3.5.1)Putchar and Getchar
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
```
The precedence value of != is greater than =, so we need to add a parentheses, in absence of parentheses c= getchar() != EOF is equivalent to c = (getchar() != EOF)

###### 3.5.2) word counting
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

#### 3.6 Arrays

An array is a collection of variables stored at contiguous memory locations.This is an example of sorting an array. First, it reads the max number of elements in the array read(n), declaration of an array  _num Array[n] the elements of the array Array[0], Array[1],..........Array[n-1].


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

#### 3.7 FUNCTIONS
Function to print the roots of the given equation.
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
    func(expression,n)
    return 0    
 ```

First we are finding the degree of the equation, read(n>-1) means degree will ask the value until the user gives a value greater than -1, _num expression[n+1] is an array of coefficients and then func:expression,n: we are calling this function to solve the roots. In the function the arguments are _num expression[], _num n and then we are defining the
_poly Eq:degree where we are storing the expression in the equation with a degree n. Now we are using an inbuilt function

x = Solve[Eq] to find the roots of the equation and using a for loop we are printing them.


#### Miscellaneous functions in GMAT

```Mathematical functions```:  	sin(x), cos(x), tan(x)  ...etc
String functions : 	
In the following, A & B are defined with _str datatype

strcpy(A,B),strcmp(A,B),strcat(A,B) ..etc

```Geometric functions``` :
In the following, A & B are defined with _polygon datatype


area(A) - returns the area of A

perimeter(A) -returns perimeter of A

numberofDiagonals(A) - returns the number of diagonals in A

numberofSides(A) - returns number of sides in A

typeofTriangle(A) - prints the type of triangle if A is a triangle, else return

center(A) - returns coordinates of center of A

orthocenter(A) - returns coordinates of Orthocenter of A if A is triangle, else return

centroid(A) - returns coordinates of Centroid of A if A is triangle, else return

circumradius(A) - returns the Circumradius of A if A is triangle, else return

circumcenter(A) - returns coordinates Circumcenter of A if A is triangle, else return

getPropeties(A) - prints all the above properties basing on polygon type of 'A'

check_Congruence(A,B) - prints "TRUE" if congruent, else "FALSE"

```Conic functions```:
 In the following A, B are defined with _conic datatype Following functions take _conic as arguments

focii(A)      - returns coordinates of focii of A

eccentricity(A) - returns eccentricity of A

focalLengh(A)    - returns focal length of A lenghofmajoraxis(A) -returns length of major axis of A

latusrectum(A) - returns length of latusrectum of A

conicProperties(A) - prints all above properties of A

typeofconic(A) - prints type of conic A is

```Polynomial functions```:

In the following A is defined with _poly B is an array of roots of a polynomial
solve(A) -returns the roots of A
getequation(A) - prints the coefficients of polynomial whose roots are in array B.

#### 3.8 Arguments- Call by value and call by reference

###### 3.8.1)Call by reference :
While calling a function, in programming language instead of copying the values of variables, the address of the variables is used it is known as "Call By References.
Program to swap two numbers
```js
add_library :+ io.LIB
swap:_num *a, _num *b: void
    _num temp
    temp = *a
    *a = *b
    *b = temp
    write(“After swapping values in the function a = ”,a,”,         b = ”, b)
main::_num
    _num a = 10, b = 20
    write(“Before swapping the the values in the main a = ”,a,”, b = ”,b)
    swap(&a,&b)
    write(“After swapping the the values in the main a = ”,a,”, b = ”,b)
```
In the above example, The variables a,b are initialized with values 10, 20. In the second line, the initial values of a and b will be printed. In the third line of the main function, we call the function swap by passing addresses of the variables a and b as arguments. The address is used to access the actual argument passed in the function call. Therefore the changes we make in the parameter will alter the passing argument.
###### 3.8.2) Call by value :

While calling a function, when you pass values by copying variables, it is known as "Call By Values."
```js
add_librabry :+ io.LIB
swap : _num a, _num b
     _num temp
     temp = a
     a = b
     b = temp
     write(“After swapping values in the function a = ”,a,”,b ”, b)

main::_num
    _num a = 10, b = 20
    write(“Before swapping the the values in main a = ”,a,”, b = ”,b)
    swap(a,b)
    write(“After swapping the the values in the main a = ”,a,”, b = ”,b)
```
In the above example, the values of the variables a and b are passed as arguments in the function call. The changes we make in parameters in the swap function will not alter the actual arguments.

Unlike call by reference, the changes made to the parameters in the function will not reflect in the actual arguments. In Call by value, actual and formal arguments will be created in different memory locations whereas in Call by reference, actual and formal arguments will be created in the same memory location.
#### 3.9 EXTERNAL VARIABLES AND SCOPE
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



## 4) ***LANGUAGE EVOLUTION***


Computational physics is the study and implementation of numerical analysis to solve
problems in physics for which a quantitative theory already exists. Different programming
languages were introduced to make these calculations easy on computers but they lacked
imperative programming which motivated us to implement our programming language gmat.

---
common programming paradigms include imperative and declarative,while some programmers
working in computational fields required both for their algorithms. imperative
programming allows the programmer to decide how to change it's state whereas in
declarative programming users could just ask for what they want as final result but
can't decide how they approach towards the answers. Coming to the programming usage of
many physicists, they needed a simple language which had imperative essence to create
general purpose algorithms and a declarative essence to play with the large data, and
enjoy single command results for already present sophisticated algorithms.

---

* Inspiring from different languages and taking user point of programming syntax is simplified and made completely user friendly.
* Large functional programming problems are simplified into smaller commands
* Overflow issues has been a user concern for many years, thus sufficient allocation of memory to the variables is completely taken care by the system.
* Dealing with large data, graph plotting, geometric analysis, algorithm implementation required different platforms whereas gmat can bring them together.
* Functinal languages are based on expressions, whereas Von-Nuemann languages were based on statements, but gmat can act on both.

gmat helps you to express your ideas more simply and clearly. gmat was built to provide mathematical software facilities, and general programming facilities with better efficiency and flexibility than other languages. The key design decisions relating to language features are made after approaching with different needs of programming refered through internet.gmat doesn't stop here, it can furthur be extend to higher dimensional analysis of data.

## 5) Examples


##  ***Example 1***
```js

~ Finding whether the given two circles are concentric,intersecting,non intersecting, touching outside,touching inside, one inside of other~


add_library:+ io.LIB
add_library:+ geo.LIB

~~defining the function check with void returntype
~~To find whethertwo circles are intersecting or not
check:_conic A,_conic B:void

    _point Centre1,Centre2

    _num dist,R1,R2

    Centre1=centre(A)

    Centre2=centre(B)

    dist=distance(Centre1,Centre2)

    R1=radius(A)
    R2=radius(B)
    if: dist==0
        write("Given two circles are concentric")
    else:

        if: dist>R1+R2
            write("Given two circles are non intersecting")
        else if: dist==R1+R2
            write("Given two circles are touching outside")
        else if: dist<R1+R2
        ~~mod is an inbuilt function to find modulus
            if: dist>mod(R1-R2)
                write("Given two circles are intersecting")
            else if: dist==mod(R1-R2)
                write("Given two circles are touching inside")
            else:
                write("one circle lies inside the other")


main::_num
    _num a1,b1,c1,h1,e1,f1
    _num a2,b2,c2,h2,e2,f2

    _conic C1=[a1,h1,b1,e1,f1,c1]
    ~~declaration of conic C1

    _conic C2=[a2,h2,b2,e2,f2,c2]
    ~~declaration of conic C2

 ~circle is an inbuilt function which takes _conic as datatype and returns '1' if given conic is circle~
    if: cirle(C1) && circle(C2)

        check(C1,C2)
        ~calling the function 'check' with C1,C2 as its parameters~

    return 0
```

##  ***Example 2***

functions - help in breaking large programs into smaller tasks

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
    write("Enter the coeficients in order:")
    for:_num i=0,i<n+1;i++
        read(expression[i])
    func(expression,n)
    return 0    


```
~~In gmat along with imperative, you will also find functional programming like Solve[] as in the above example.
~~function syntax ==> function_name:arguments:return_types

```js

func:_str expression _num degree:
    _poly Eq:n
    Eq = [expression]
    _num x[n]
    x = Solve[Eq]
    for:_num i=0,i<n:i++
        write(x[i]," ")
    write("\n")

main::_num
    _num n
    write("Enter the degree of equation:")
    read(n>-1)

    _num expression[n]
    write("Enter the coeficients in order:")
    for:_num i=0,i<n;i++
        read(expression[i])
    func(expression,n)   
    return 0

```
~~arguments and return_types(if present) must be seperated by commas.

~~variable 'n' is defined in main function; It cant be accessed in the function outside the main. scope of variable 'n' is from the place where it is defined till the end of main function only.

~~Enough number of variables must be provided for the Solve[] function, lesser number of variable would throw an error in the programming.   

##  ***Example 3***

~~calculating angle between two lines

```js
add_library :+ io.LIB

angle : Line1,Line2 : _num
    _num m1,m2
    m1 = (y2-y1)/(x2-x1)
    m2 = (y4-y3)/(x4-x3)
    _num a1,a2,a3
    a1 = tanIn(m1)
    a2 = tanIn(m2)
    if: (a2-a1)>=0
        a3 = a2-a1
    else
        a3 = a1-a2
    write(“Angle between given two lines is ”,a3,“ radians”)

main :: _num

    _num x1,y1,x2,y2,x3,y3,x4,y4
    _line Line1,Line2
    write(“Give coordinates of two edges of the first line(in order x1,y1,x2,y2):”)
    read(x1,y1,x2,y2)
    Line1 = [x1,y1;x2,y2]
    write(“Give coordinates of two edges of the second line(in order x1,y1,x2,y2):”)
    read(x3,y3,x4,y4)
    Line2 = [x3,y3;x4,y4]
    angle(Line1, Line2)
    return 0
```

##  ***Example 4***
~tangent from the given point

```js
add_library :+ io.LIB

main :: _num

_conic C
_num x1,y1
_num a,h,b,g,f,c
write(“Give coefficients of the conic:”)
read(a,h,b,g,f,c)
C.inject(a,h,b,g,f,c)
write(“Give the coordinates of the point:”)
read(x1,y1)
_num s11 = (a*x1*x1)+(2*h*x1*y1)+(b*y1*y1)+(2*g*x1)+(2*f*y1)+c
if: s11==0
    write(“Given point lies on conic and has only one tangent at that point”)
else if: s11>0
    write(“Given point lies outside conic and has 2 tangents passing through it”)
else
    write(“Given point lies inside conic and has 0 tangents through it”)
```

##  ***Example 5***

* Using string data-type

```js
~~single line comment
~multi line comment~

~syntax to add libraries ==> add_library :+ 'library name'~
add_library :+ io.LIB
~NOTE: there should be no space between : and + ~

~function format ==> function:arg1,arg2:ret_type1,ret_type2 ~
~if more than one argument or return type, you need to place a "," in between~
main::_num
  _str x    
  x = "hello world 2.0"  
~string data type is used to store a sequence of characters ~
  write(x)
~write function prints everything stored in the variable ~
  return 0
```

## ***Example 6***

* This example focuses on Syntax of loops

```js
add_library :+ io.LIB

main:: _num
~variables can be declared and initialised at same time~
~Gmat usesindentation;extra tab space is to be added at beggining of function/loops~
  _num a=0,r=0,n=0
~by default variables are initialised to 0 and pointers are initialised to NULL~
  read(a,r,n)
  _num A[n]

~for loop syntax ==> for:initialize,termination:increment/decrement~  
  for:_num(i=0),i<n:i++
     A[i] = a*pow(r,i)

~while loop syntax ==> while:condition~
  _num j=0
  while:j<n
    _num temp = A[j+1]
    A[j+1] = A[j]
    A[j] = temp
    j++

  write(A)
  return 0
```

## ***Example 7***

* Finding roots of a quadratic equations

```js
~ finding roots for a quadratic equation ~
add_library :+ io.LIB
add_library :+ geo.LIB

main::_num

~_poly is the data type to define the polynomial equations with degree~
~_num is a type specifier
  it includes all four basic arthematic type specifiers in C
  It uses dynamic binding to allocate space to the declared variable~
  _poly Eq:2
  _num a, b, c  
~if not initialised all variables are set to Zero~  
~write(a,b,c)  --> at this point would give out 000 as output~

  write("input co-eff of quad")
  read(a,b,c)
~inserting the coefficients to the equation~
  Eq = [a,b,c]
  _num x,y

~solve(polynomial equation | variable) gives the roots of the equation written
    note that if b^2-4a*c<0 ; 'und - undefined' will return into x,y ~


  (x,y) = solve(Eq)
  write("roots are:",x,"and",y)
  return 0
```

## ***Example 8***

* Intro to polygon datatype and plotting

```js
~Finding centroid of the polygon~
add_library :+ io.LIB
add_library :+ plotG.LIB
~plotG.LIB library allows you to open plot windows/tabs~

main :: _num
  write ("Enter the coordinates of the triangle:")
  _num x1, y1, x2, y2, x3, y3
  read(x1,y1,x2,y2,x3,y3)

~input to polygon, given in the form of points~
~polygon is a datatype, used to store end point co-ordinates of polygon~
  _polygon A = [x1,y1;x2,y2;x3,y3]

~three points that is triangle is given as input~
~side_len() returns the sidelengths of the polygon~
  _num a,b,c
  (a,b,c) = side_len(A)
~(...arg) = side_len(A) number of arguments should not be less~
  write(a,b,c)
~prints all sides of polygon A ~

~ finding the type of the triangle(acute/right/obtuse) ~
  _str B = type[triangle(A)]
~type[] returns a string, donot store the value in _num type variables~

  _num x4,y4
  (x4,y4) = centroid(A)
~() = centriod(A) ; make sure correct number of arguments are provided and they are enclosed by brackets~

  write("A is ")
  write(B,"\n")     ~ \n for new line
  write("Centroid of the triangle : ")
  write("(",x4,",",y4,")")
~plotting the polygon on a 2D plane~
  Plotgraph[polygon(A),centroid(A)]
  return 0

```

##  ***Example 9***

* Variable Naming and declarations

```js
add_library :+ io.LIB

~Variable Naming and declarations~

main::_num
    _num variable_12      ~~ Declaring a variable_12

    ~~ variables names can contain letters and digits.
    ~~ Variable name starts with alphabets.
    ~~ Gmat is case sensitive .

    variable_12 = 15

    ~~ assigning of variable can be done while declaration also

    write(variable_12)


    return 0
```

* OUTPUT:
    15

    ~NOTE:

    keywords should not be used as variable names

    _num if

    _num switch ... will give ERROR in the OUTPUT


##  ***Example 10***

* Datatypes

```js
~Datatypes~

add_library :+ io.LIB

main::_num

    _num x1 = 5 ,y1 = 5.5
    _num x2 = 10.5, y2 = 10.5
    _num x3 = -12.25, y3 = -6

    _str y = {'a','e','3'}  

    _point p1,p2

    p1 = [x1,y1]
    p2 = [x2,y2]
    p3 = [x3,y3]

    _polygon A = [p1;p2;p3]
    ~A is a triangle ~
    ~A can be also defined in this way "A = [x1,y1;x2,y2;x3,y3]"  ~


    _conic var

    var.inject(1,0,1,0,0,-9)

    ~conics general equation ax^2+2hxy+by^2+2gx+2fy+c~
    ~Here var is a circle with centre origin and radius 3 ~

    _poly Eq:3
    ~This implies Eq is a polynomial with degree 3~
    Eq = [1,-3,3,-1]
    ~~ 1,-3,3,-1 are coefficients of polynomial

    return 0

~~ _num allocates memory according to the value assigned to the variable
~~ _str datatype is used to store charaters and strings
~~ _point datatype is used to store coordinates
~~ _polygon takes co-ordinates as input
~~ _conic datatype takes the coefficients of the equation defining conic as input.Coefficients must be given in the order [a,h,b,g,f,c] where
ax^2+2hxy+by^2+2gx+2fy+c is the general equation of conics.
~~_poly datatype takes the coefficients of polynomials as inputs and return the roots of the polynomial equation(if roots are imaginary it returns "und")    
~~_polygon , _conic, _poly datatypes input is given inside "[]" these brackets only.
```

##  ***Example 11***

* Arthimetics operators:  +,-,*,/,%  

```js
add_library :+ io.LIB

main::


    ~~precedence order is same as in all languages
    ~~ parsing is done from left to right

    _num x=0,y=0

    x = 3+4*5/2*8%2
    y = 3+4/2*5+8%3

    write(x," ",y)

    return 0
```

* OUTPUT:
3 15

~ 3+4* 5/2*8%2

   3+20/2*8%2

   3+10*8%2

   3+80%2

   3+0

   3~

~ 3+4/2*5+8%3

  3+2*5+2

  3+10+2

  13+2

  15~

~~ +,- have same precedence

~~ *,/,% have same precedence

~~ precedence(*,/,%) > precedence(+,-)

##  ***Example 12***

* logical and relational operators  

```js
add_library :+ io.LIB

~logical and relational operators ~

~relationl operaters: <,=<,>,>=,@ ~
~logical operators: ==, != ~

main::_num

    _num y=20,z=30

    _num variable
    write("give input number:")
    read(variable)

    ~RELATIONAL OPERATORS~
    if: variable <= y
    write(variable,"is less than or equal to ",y,"\n")


    else if: variable@(y,z]
    write(variable,"lies in the interval (",y," ,",z,"]","\n")

    else
    write(variable,"is greater than ",z,"\n")

    ~LOGICAL OPERATORS~

    _num x,y

    write("Enter two numbers:")
    read(x,y)

    if: x==y    
        write("given inputs are equal")
    else:
        write("given inputs are not equal")    



    return 0
~~operators(<,>,<=,>=) have equal precedence
~~operator '@' has more precedence
~~operators(==,!=) have equal precedence
~~Logical operators have lower precedence than relational operators
~~NOTE:
~~   variable@(x,y)   --checking if variable is in between x,y
~~   variable@(x,y]   --checking if variable is in between x,y with y inlcuded in the range
~~   variable@[x,y)   --checking if variable is in between x,y with x inlcuded in the range
~~   variable@[x,y]   --checking if variable is in between x,y with x and y inlcuded in the range
```

* INPUT1:
34
10 12

* OUTPUT1:
34 is greater than 30
given inputs are not equal

* INPUT2:
26
-14.5 14.5

* OUTPUT2:
26 lies in the interval (20,30]
given inputs are not equal

* INPUT3:
7
12.55 12.55

* OUTPUT3:
7 is less than or equal to 20
given inputs are equal


##  ***Example 13***

* Bitwise operators

```js
add_library :+ io.LIB

main::_num

  _num x = 7
  _num y = 9

  _num z = x ^ y            ~~bitwise xor
  write(z,"\n")

  z = x & y                        ~~bitwise and
  write(z,"\n")

  z = x | y                        ~~bitwise or
  write(z,"\n")

  z = x << y                    ~~leftshift
  write(z,"\n")

  z = x >> y                    ~~rightshift
  write(z,"\n")

  z = $x                            ~~negation
  write(z,"\n")

  return 0
```

* OUTPUT:
14
1
15
3584
0
-8


##  ***Example 14***

* assignment operators , increment and decrementers

_num x,y,z

x++ demonstrates same as x = x+1 also x++ is equal to x++1

general arithmetic operators
x++y demonstrates x = x+y
x--y demonstrates x = x-y
x**y demonstrates x = x*y
x//y demonstrates x = x/y

x += y demonstrates x = x+y
x -= y demonstrates x = x-y
x *= y demonstrates x = x*y

x &= y demonstrates x = x & y

in general expr1 op= expr2 demonstrates expr1 = (expr1) op (expr2) where op is any operator

while expr1 op op expr2 demonstrates expr1 = (expr1) op (expr2) where op is only arithmetic operator


### ***Example 15***
```js
add_library :+ io.LIB


main::_num

_num p=2,n=1
_num x=7
_num y= (x >> (p+1-n)) & $(2 << n);

if:y
    write("condition1 is satisfied!!")
if:5^3+4/2*3%2&6@[6,10)
    write("condition2 is satisfied.")    

return 0
```



OUTPUT:
condition1 is satisfied!!

condition2 is satisfied.


##  ***Example 16***

* If - Else if

```js
add_library :+ io.LIB

main::_num

    _num BMI,ht,wt
    write("Enter your height(in m) and weight(in kg) respectively:")
    read(ht,wt)

    BMI= wt/(ht*ht)
    write((0.2)BMI)

    if: BMI < 18.5
        write("Underweight\n")
    else if : BMI@[18.5,25)  ~BMI lies between [18.5,25)~
        write("Normal\n")
    else if : BMI@[25,30)   
        write("Overweight\n")
    else :
        write("Obesity\n")

    return 0
```

* EXAMPLES:

INPUT1:
1.64 50

OUTPUT1:
18.59
Normal

INPUT2:
1.67 74

OUTPUT2:
26.53
Overweight

##  ***Example 17***

* switch case

```js
add_library :+ io.LIB

main::_num

    _num N
    write("Enter the number of verices of a polygon:")
    ~N should be postive~
    read(N>0)
    ~~read function prompts the user till user enters valid input(special feature)
    ~~write function also follows the same

    switch : N
        case : 1 : write("point\n")
                   break
        case : 2 : write("line\n")
                   break
        case : 3 : write("triangle\n")
                   break
        case : 4 : write("quadrilateral\n")
                   break
        case : 5 : write("pentagon\n")
                   break
        case : 6 : write("hexagon\n")
                   break
        case : 7 : write("heptagon\n")
                   break
        case : 8 : write("octagon\n")
                   break
        case : 9 : write("nonagon\n")
                   break
        case : 10 : write("decagon\n")
                   break           
        default : write(N,"-sided polygon")           
    ~Implement range in switch case~

    ~Can be implemented for strings as well~
    return 0
```

* EXAMPLES:

Input1:
4

Output1:
quadrilateral

Input2:
-3 (Since, the given input is invalid, it won't be considered, so user should enter - speciality of read function)
7 (It will be considered, since it is valid input)

output2:
heptagon


##  ***Example 18***

* for loop

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

* EXAMPLES:

INPUT1:
10
3 7 9 5 10 6 1 4 2 8

OUTPUT1:
1 2 3 4 5 6 7 8 9  10

INPUT2:
5
-2 0.05 1.4 2.6 -3.2

OUTPUT2:
-3.2 -2 0.05 1.4 2.6

##  ***Example 19***

* while loop

```js
add_library :+ io.LIB
add_library :+ geo.LIB
add_library :+ plotG.LIB

main::_num

    _polygon T
    _num x1,x2,x3,y1,y2,y3

    write("Enter the coordinates of the triangle:")
    read(x1,y1,x2,y2,x3,y3)
    T=[x1,y1;x2,y2;x3,y3]

    while: Area(T) > 10  
        Plotgraph [T]
        write(Area(T))
        T=Medialtriangle(T)
        ~Medial triangle is triangle formed with mid points of the sides as new vertices ~

    return 0
```

* EXAMPLES:

INPUT1:
-3 10 -3 -8 9 -8

OUTPUT1:
(Figure will be plotted)
108
27

##  ***Example 20***

* jump(goto)

```js
add_library :+ io.LIB

main::_num

    _poly Eqn:2
    _num x,y

    Eqn = [a,b,c]

    Label:

    write("Enter the coefficients of the equation:")
    read(a,b,c)

    (x,y) = Solve(Eqn)
    write("Roots:",(0.3)x,",",(0.3)y)


    if: x==y
        write("Roots are equal\n")
    else:
        write("Roots are not equal\n")
        jump Label

    return 0
```

* EXAMPLES:

INPUT1:
4 -12 9

OUTPUT1:
Roots:1.50,1.50
Roots are equal

INPUT2:
2 -5 2
3 -10 4
9 -6 1

OUTPUT2:
Roots:0.500,2.000
Roots are not equal
Roots:0.464,2.868
Roots are not equal
Roots:0.333,0.333
Roots are equal



##  ***Example 21***

* Scope of variables
The scope of a name is the part of the program within which the name can be used


```js
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
~~the "y"-variables here prints the value stored in the 'y' outside the forloop
    return 0
INPUT:
5
```

OUTPUT:
1 2 3 4 5
10 5

##  ***Example 22***

functions - help in breaking large programs into smaller tasks

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
    write("Enter the coeficients in order:")
    for:_num i=0,i<n+1;i++
        read(expression[i])
    func(expression,n)
    return 0    



~~ In gmat along with imperative, you will also find functional programming like Solve[] as in the above example.
~~function syntax ==> function_name:arguments:return_types
```
```js

func:_str expression _num degree:
    _poly Eq:n
    Eq = [expression]
    _num x[n]
    x = Solve[Eq]
    for:_num i=0,i<n:i++
        write(x[i]," ")
    write("\n")

main::_num
    _num n
    write("Enter the degree of equation:")
    read(n>-1)

    _num expression[n]
    write("Enter the coeficients in order:")
    for:_num i=0,i<n;i++
        read(expression[i])
    func(expression,n)   
    return 0

```
~~arguments and return_types(if present) must be seperated by commas.

~~variable 'n' is defined in main function; It cant be accessed in the function outside the main. scope of variable 'n' is from the place where it is defined till the end of main function only.

~~Enough number of variables must be provided for the Solve[] function, lesser number of variable would throw an error in the programming.   

## ***Example 23***

* Header Files ,Libraries
io.LIB, geo.LIB, plotG.LIB are some examples of header files in gmat

```js
add_library :+ io.LIB
main::_num
    _str name[20]
    write("Enter your name:")
    read(name)

    write("hello",name," welcome to gmat programming!!")
```

INPUT:
xlr8

OUTPUT:
hello xlr8 welcome to gmat programming!!

~~ io.LIB library contains the standard input output functions like write(),      read()...etc
~~ geo.LIB contains the geometric functions
~~ plotG.LIB helps you to plot the geometric data
~~ without the libraries, for the code to run you need to write the functions     yourself!!

## ***Example 24***

```js
add_library :+ io.LIB

main::_num
    _num x = 5
    static _num cr = 7

    for:_num x,x<10:x++
        write(x," ")
    write("\n")    
    write(x,"\n")
    write(cr)
return 0
```

OUTPUT:
0 1 2 3 4 5 6 7 8 9
5
7

~~ declared variables are initialised to zeroes by default
~~ As the for-loop is done, the variable x inside the scope of for-loop gets destroyed
~~ the value inside x will still be 5, the variable x inside the for-loop is not same as the outer one as  new declaration  '_num x ' was done.

## ***Example 25***

* Recursion and static variables

```js
add_library :+ io.LIB

fib:_num argument:_num
    static _num var = 0 ;
    var+=1
    write(var,"(",x,") ")
    if(argument == 1 || argument ==2)
        return 1
    return fib(n-1)+fib(n-2)


main::_num
    write("Enter the number:")
    _num x
    read(x)

    _num a
    a = fib(x)
    write("/n")
    write("fibonocci number = ",a,"\n")
```

INPUT:
6

OUTPUT:
1(6) 2(5) 3(4) 4(3) 5(2) 6(1) 7(2) 8(3) 9(2) 10(1) 11(4) 12(3) 13(2) 14(1) 15(2)
fibonocci number = 8

~~Function syntax ==> function:arg1,arg2...:ret_type1,ret_type2....
~~static varaibles preserve their values in their scope, and are not initialised again in their new scope

## ***Example 26***

* gmat preprocessors
~~ add_library , define are two preprocessors of gmat
~~ instead of standard libraries like io.LIB, geo.LIB gmat allows you to write create your own libraries. you can add them either statically or dynamically.

new.LIB
#ifndef LIB_FILE
#define LIB_FILE
comparision:arguments:_num
#endif

new.gm
~~ contains the required type of comparision function
```js
comparision:_str x[],_str y[]:_num
    _num i = 0
    while:x[i]!='\0' && y[i]!='\0'
        if:x[i]<y[i]
            return 1
        else if:x[i]>y[i]
            return -1
    if:x[i]=='/0' && y[i]=='/0
      return 0
    else if: x[i]=='/0'
      return 1
    else
      return -1          
return 0
```

```js
add_library :+ io.LIB
add_library :+ new.LIB
main::_num
    ~~ here you can now directly call the comparision function
    _str array1[], array2[]
    write("Enter the two strings:")
    read(array1,array2)
    write(comparision(array1,array2))
return 0
```

INPUT:
abcdef abcder

OUTPUT:
1

INPUT:
qwerty qwe

OUTPUT:
-1

~~ #ifndef -makes sure that LIB_FILE is defined only once


## ***Example 27***

```js
add_library :+ io.LIB

~~only for printing

main :: _num

        _num x = 10
        write(x,"\n")

        _str s = "this is a string"
        write(s,"\n")

    _poly Eqn:2
    _num x,y
    ~~ equation with degree 2: a*x*x + b*x + c
    _num a = 1 , b = 5 , c = 6

    Eqn = [a,b,c]

        (x,y) = Solve(Eqn)
    ~~ prints the roots of the equation x,y
    write("Roots:",x,",",y)

      return 0
```


output:

10

this is a string

Roots:-2,-3

## ***Example 28***

```js
add_library :+ io.LIB
add_library :+ geo.LIB

main :: _num

    _polygon T
    _num x1 = 0,x2 = 8,x3 = 0,y1 = 0,y2 = 0,y3 = 8

    T=[x1,y1;x2,y2;x3,y3]
  ~~prints the properties of the polygon T
    write(getproperties(T))

    return 0
```


output:

This is a right angled isosceles triangle

sides are 8,8,11.3137

centroid:{2.666,2.666}

orthocentre:{0,0}

circumradius:5.65685

circumcentre:{4,4}

incentre:{2.34315,2.34315}

inradius:2.34315

altitude(from hypotenuse):5.65685

perimeter:27.3137

area:32 sq.units

## ***Example 29***

```js
add_library :+ io.LIB

main::_num
    _num n
    write("enter a number n:")
  ~~ reads the value of n
    read(n)
  ~~ prints the square of the number(n)
    write("the square of the number ",n," is:",n*n,"\n")

    _str s
    write("enter a string:")
  read(s)
    for:_num(i=0),i++:i<n:
        write(s,"\n")

return 0
```


OUTPUT:

enter a number n:5

the square of the number 5 is:25

enter a string:This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

## ***Example 30***

```js
add_library :+ io.LIB
add_library :+ geo.LIB

~~formatted input/output

main::_num

    _num x,r,c
    write("enter the number x: ")
    read((0.3)x)
    write("number entered is: ",x,"\n")

    write("enter the radius r: ")
  ~~reads the value of r
    read(r)
  ~~prints the formatted value of r
  ~~decimal part of r value is rounded off to 3 digits
    write("radius entered: ",(0.3)r,"\n")
  ~~getcircumference calculates the circumference of the circle with radius r
    c = getcircumference(r)
  ~~decimal part of circumference value is rounded to 5 digits
    write("circumference of the formed circle: ",(0.5)c,"\n")

    _str s
    write("enter the string:")
    read(s)

  ~(a.b.c) prints a formatted string- (a) spaces at the beggining, (c) spaces at the end and (b) is the max no.of characters it can print~

    write("the entered string is: ",(6.7.10)s,":")


  return 0
```

OUTPUT:

enter the number x: 8.3975345

number entered is: 8.398

enter the radius r: 5.674599

radius entered: 5.674

circumference of the formed circle: 35.65456

enter the string:Hello,world

the entered string is: (6_spaces)hello,w(10_spaces):


## ***Example 31***

```js
~~file access

add_library :+ io.LIB
add_library :+ geo.LIB

 main::_num
    _num a,b,c,d,distance
    ~~ datatype _point, which is the cordinate of point(x,y)
    _point p1,p2
    ~~Declaration of file pointer
    FILE *fp, *fpr
    ~~ Opening the files
    fp = fopen(input.txt, "r")
    fpr = fopen(output.txt, "w")
    ~~ reads the input fro input.txt file
    fread(fp,a,b,c,d)
    ~~ assining the points and calculating the distance between them
    p1 = [a,b], p2 = [c,d]
    distance = getdistance(p1,p2)

    ~~ prints the distance between points in the output.txt file
    fwrite(fpr,"The distance between the given points is ", distance)

    ~~close the files
    fclose(fp)
    fclose(fpr)
    return 0;
```


INPUT FILE

input.txt
1 2
3 4


OUTPUT FILE

output.txt
The distance between the given points is 1.414

## ***Example 32***

* Miscellaneous functions

Mathematical functions (sinx,cosx,tanx...etc)

String functions(strcpy,strcmp,strcat..etc)

Geometric functions:

In the following, A,B are defined with _polygon datatype

Following functions take _polygon as arguments

area(A)             -returns area of A

perimeter(A)        -returns perimeter of A

numberofDiagonals(A)-returns number of diagonals in A

numberofSides(A)    -returns number of sides in A

typeofTriangle(A)   -prints the type of triangle if A is
                     a traingle, else return

center(A)           -returns coordinates of center of A

orthocenter(A)      -returns coordinates of Orthocenter
                     of A if A is triangle, else return

circumradius(A)     -returns the Circumradius of A if A
                     is triangle, else return

circumcenter(A)     -returns coordinates Circumcenter
                     of A if A is triangle, else return

getPropeties(A)     -prints all the above properties
                     basing on polygon type of 'A'

check_Congruence(A,B)-prints "TRUE" if congruent,else   
                     "FALSE"

Conic functions:

In the following A,B are defined with _conic datatype

Following functions take _conic as arguments

focii(A)             -returns coordinates of focii of A

eccentricity(A)      -returns eccentricity of A

focalLengh(A)        -returns focal length of A

lenghofmajoraxis(A)  -returns length of majoraxis of A

latusrectum(A)       -returns length of latusrectum of A

conicProperties(A)   -prints all  above properties of A

typeofconic(A)       -prints type of conic A is

Polynomial functions:

In the following A is defined with _poly,
B is an array  of roots of a polynomial

solve(A)             -returns the roots of A

getequation(B)       -prints the coeffients of
                      polynomial whose roots are in array B

```js
add_library :+ io.LIB

main::_num

    _point pt1, pt2, pt3
    _polygon T
    write("Enter the coordinates of the triangle in the order (x1,y1), (x2,y2), (x3,y3) : ")
    read(pt1,pt2,pt3)
    T = [pt1, pt2, pt3]

    typeofTriangle(T)
    write("\nPerimeter of the triangle is ",(0.2)Perimeter(T))
    write("\nArea of the triangle is ",Area(T))
    _num x,y = Center(T)
    write("The centrid of the triangle ",(0.2)x," ",(0.2)y)
    x,y = Circumcenter(T)
    write("The Circumcenter of the triangle ",x," ",y)
    return 0
```


OUTPUT :

Enter the coordinates of the triangle in the order (x1,y1), (x2,y2), (x3,y3) : 0 0 8 0 0 8

Triangle is a right angled triangle

Perimeter of the triangle is 27.31

Area of the triangle is 32

The centrid of the triangle 2.67 2.67

The Circumcenter of the triangle 4 4


## ***Example 33***

```js
add_library :+ io.LIB
add_library :+ geo.LIB

class comparestrings
      private:
            _str a,b

      public:
        comparestrings::
            comparestrings:x,y:void
                a = x,b = y

            void injectstrings:x,y:void
                a = x,b = y

            compare::
                  if:a>b
                  write(a,"is greater string","\n")
                  else:
                  write(b,"is greater string","\n")

        write_string::
            write(a,b,"\n")


main :: _num
        ~~ class is created with default constructor
        comparestrings comparision1:"this example ","is to demostrate classes"


    comparestrings xyz



        comparision1.write_string


        ~~class is being created
        comparestrings comparision2
        ~~using functions in the class to use other functions
        comparision2.injectstrings("this is ","second example")
        comparision2.compare:
        comparision2.write_string:
```

output:
this example is to demonstrate classes
this is  is the greater string
this is second example

~~private: cant be accessed outside the class
~~public: can be accessed outside class

###    ***EXAMPLE 34***

* explaining multiple Inheritance: A class being derived from more than one base class.

```js

add_library :+ io.LIB
add_library :+ geo.LIB

class parentA
    public:
        parentA::
            write("constructer of A is called.\n")
        getperimeter:_polygon x:
            write(perimeter(x),"\n")
class parentB
    public:
        parentB::
            write("constructer of B is called.\n")
        getarea:_polygon x:
            write(area(x),"\n")

class childC: import public parentA, import public parentB
    public:
        childC::
            write("constructer of C is called.\n")
        getcentriod:_polygon x:
            write((0.3)centriod(x))

main::_num
    childC variable
    _polygon triangle = [0,0,6,0,0,8]

    variable.getcentriod(triangle)
    varaible.getarea(triangle)
    varaible.getperimeter(triangle)

```
OUTPUT:

constructer of A is called

constructer of B is called

constructer of C is called

2 2.67

24

24

* class childC: import public parentB, import public parentA
* if this was the order, constructer of B would be called first and then of A


## ***Example 35***  


```js
~~polymorphism

~~function overloading in GMAT


add_library :+ io.LIB


printpretty:_num number:_num
    write(number,"is of type ",typeof(number),"\n")

printpretty:_str somestring:_str
    write("\"",somestring,"\"is of type ",typeof(somestring),"\n")


main::_num

    _num number
    write("enter some number: ")
    read(number)
    printpretty:number:


    _str s
    printpretty(number)
    write("enter some string: ")
    read(s)
    printpretty:s:

    return 0
```


OUTPUT:
enter some number: 10.445
10.445 is of type number

enter some string: This is gmat language
"This is gmat language" is of type string_literal


## ***Example 36***


```js
add_library :+ io.LIB
add_library :+ geo.LIB

catch:_str x:
    if:x
    write("invalid exception caught! at level ",level(throw),"\n")

class mainclass
        private:
            _num numerator,denominator

        public:
                mainclass::
                mainclass:num,denom:
                    numerator = num
                    denominator = denom

                _num divide::
                        if:denominator = 0 throwexpt:invalid
                        return numerator/denominator


main :: _num

    mainclass divisionclass
    _num x,y,result
    write("enter numerator: ")
    write("enter denominator: ")
    divisionclass:x,y:
    result = divisionclass.divide:
    write("result is :",result,"\n")

    mainclass divisionclassprime(17,0)
    result = divisionclassprime.divide:
    write("result is :",result,"\n")
```


OUTPUT:
enter numerator: 5
enter denominator: 12
result is : 0.4166667

invalid exception caught at level divide in mainclass type


## ***Example  37***

* operater overloading
* gmat allows you to have more than one defination for an operater in the same scope

```js
add_library :+ io.LIB

class complex
    private:
        _num real,imag
    public:
        complex::
        complex:_num ireal,_num iimag:
            real = ireal
            imag = iimag
        operater +:complex x:complex
            complex temp
            temp.real = real + x.real
            temp.imag = imag + x.imag
            return temp

        print::
            write(real,"+",imag,"i\n")

main::_num
    complex c1(2,3)
    complex c2(3,4)

    complex c3
    c3 = c1+c2
    c3.print::
    return 0
```
OUTPUT:

5+7i

## ***Example 38***

* pointers and addresses

```js
add_library:+ io.LIB

main::num
  _num a,b, *ip, A[10]
  write("Enter the value of a: ")
  read(a)
  ~~ ip stores the address of a
  ip = &a
  ~ b gets the value stored in the address that ip is pointing to ~
  b = *ip
  (*ip)++3
  ~~ *ip is a
  ~~ (*ip)++3 is in the format x++y => x=x+y, which means a=a+3
  write("\naddress of a is :",ip)
  write("\nnew value of a is",a)
  write("\nb value is",b)
  ~~ now ip stores the address of the array
  ip = &A[0]
  ~~ Now with ip, whole array can be accessed
  ~~ *(ip+1), *(ip+2) => A[1],A[2]
  write("\naddress of A[5]: ",ip+5)
  return 0
  ```


  OUTPUT :

  a value: 3

  address of a is : 217564

  new value of a is 6

  b value is 3

  address of A[5]: 265389


## ***Example 39***

* pointers in function arguements

```js
add_library:+io.LIB

main::_num
  _num n
  write("enter degree of the equation :")
  read(n)
  _num Arr[n]
  write("\nenter the roots of the equation ")
  for:_num (i = 0),i<n:i++
    read(Arr[i])
  ~~In the function the argument is a pointer (*Arr)
  write("\ncoefficients of the equation are: ",)
  getequation(*Arr)
  return 0
```



  OUTPUT 1:
  enter degree of the equation : 3
  enter the roots of the equation 1 2 3
  coefficients of the equation are: 1 -6 11 -6

  OUTPUT 2:
  enter degree of the equation : 2
  enter the roots of the equation 21 -5
  coefficients of the equation are: 1 -16 -105


## ***Example 40***

* pointers and arrays

```js
add_librabry:+io.LIB
~~ function:function arguments:return type
~~ function arguments are pointers
search: void *array, _num arr_size, _num element:_num
  for:_num(i=0),i++:i<arr_size:
    if : array[i] == element
      return 1
  return 0  

main::_num
  _num n,element
  write("size of the array:")
  read(n)
  _num Array[n]
  for:_num(i=0), i++:i<n
    read(A[i])
  write("enter the value to be searched: ")
  read(element)
  ~~ function(function arguments)
  _num value = search(*Array,n,element)
  if : value == 1
    write("given",element,"is in the array")
  else
    write("given",element,"is not in the array")
return 0
```


OUTPUT 1:

size of the array: 5

3 4 1 6 0

enter the value to be searched: 4

4 is in the array


OUTPUT 2:

size of the array: 10

34 21 7 4 53 0 27 18 2 76

enter the value to be searched: 100

100 is not in the array

## ***Example 41***

* string pointers

```js
add_librabry:+io.LIB
add_librabry:+str.LIB

main::_num
_str *A ={"hello world!","This is gmat","Popl project"}
~~A is a string pointer like array of strings
~~It stores value dynamically
~Initialization must be in the format same as above i.e, A={"string1","string2",...."stringn"}~
strcpy(A[3],A[1])
~A[3] can also be accessed even the Initialization is upto A[2]~
write("2nd string : ",)
write("\nenter the 5th string: ")
read(A[4])
if : strcmp(A[1],A[3]) == 0
  write("\nstrings 2nd and 4th strings are same")
else
  write("\nstrings 2nd and 4th are not equal")

strcat(A[2],A[3])
write("\n3rd string is : ",A[2])
return 0
```


OUTPUT:

2nd string : This is gmat

enter the 5th string: Gmat programming language

strings 2nd and 4th strings are same

3rd string is : Popl projecthello world!

## ***Example 42***

* string pointers

```js
add_librabry:+io.LIB
add_librabry:+str.LIB

main::_num
_str *A ={"hello world!","This is gmat","Popl project"}
~~A is a string pointer like array of strings
~~It stores value dynamically
~Initialization must be in the format same as above i.e, A={"string1","string2",...."stringn"}~
strcpy(A[3],A[1])
~A[3] can also be accessed even the Initialization is upto A[2]~
write("2nd string : ",)
write("\nenter the 5th string: ")
read(A[4])
if : strcmp(A[1],A[3]) == 0
  write("\nstrings 2nd and 4th strings are same")
else
  write("\nstrings 2nd and 4th are not equal")

strcat(A[2],A[3])
write("\n3rd string is : ",A[2])
return 0
```


OUTPUT:

2nd string : This is gmat

enter the 5th string: Gmat programming language

strings 2nd and 4th strings are same

3rd string is : Popl projecthello world!


## ***Example 43***

* pointer arrays

```js
add_library :+ io.LIB
add_library :+ geo.LIB

main::_num

    _num n
    write("Enter the number of coordinates:")
    read(n)

    _polygon *Tri[3]
    ~~array of pointers that points to triangles

    _point pt[6]
    ~~ pt is an array of coordinates

    for : _num(i=0),i++:i<n
        _num x,y
        read(x,y)  ~~taking input from user
        ~incorrect format for taking point as input~
        pt[i] = (x,y)


    for : _num(i=0),i++:i<3
        ~incorrect format for rand~
        _num j = rand % n  
        if: j+2 < n    
            *Tri[i] = [pt[j];pt[j+1];pt[j+2]]
      ~Tri[i] stores the address of a triangle formed by 3 consecutives coordinates in the array~
        else:
            i--

    Check_Congruence(Tri[0],Tri[1])
    Check_Congruence(Tri[1],Tri[2])
    Check_Congruence(Tri[2],Tri[0])
    ~~Check_Congruence is a function with 'polygon' as arguements

    return 0
```


OUTPUT :

line:22:error : pt[i] = (x,y) : (incorrect brackets)

line:27:error:_num j = rand % n  :(incorrect format, expecting a bracket)

line:34:error:Check_Congruence(Tri[0],Tri[1]) : (wrong arguement was entered)

line:35:error:Check_Congruence(Tri[1],Tri[2]) : (wrong arguement was entered)

line:36:error:Check_Congruence(Tri[2],Tri[0]) : (wrong arguement was entered)


## ***Example 44***

* multidimensional array
  addition of two matrices

```js
add_library :+ io.LIB

main::_num

    _num m,n
    write("Enter the order of matrices to be added:")
    read(m,n)

    _num Mat1[m][n],Mat2[m][n], Sum[m][n]
    ~Mat1,Mat2,Sum are 2 dimensional arrays initialised with '_num' datatype~
    ~Similarly, Mat1[i][j][k] is a 3d array


    write("Enter the elements of 1st matrix:\n")

    ~~Taking input of 1st mtrix from user
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            write("Enter Mat1[",i,"]","[",j,"] value:")
            read(Mat1[i][j])


    write("Enter the elements of 2nd matrix:\n")

    ~~Taking input of 2nd mtrix from user
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            write("Enter Mat2[",i,"]","[",j,"] value:")
            read(Mat2[i][j])

    ~~adding both matrices
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            Sum[i][j]=Mat1[i][j]+Mat2[i][j]

    write("Resultant Matrix:")

    ~~printing Resultant matrix
    for:_num(i=0),i++:i<m
        write("\n")
        for:_num(j=0),j++:j<n           
            write("Sum[i][j] ")

    return 0
```



    OUTPUT:
    Enter the order of matrices to be added:2 3
    Enter the elements of 1st matrix:
    Enter Mat1[0][0] value: 10
    Enter Mat1[0][1] value: -2.3
    Enter Mat1[0][2] value: 5
    Enter Mat1[1][0] value: 6.67
    Enter Mat1[1][1] value: 9
    Enter Mat1[1][2] value: -7
    Enter the elements of 2nd matrix:
    Enter Mat2[0][0] value: -3
    Enter Mat2[0][1] value: -3.4
    Enter Mat2[0][2] value: 8
    Enter Mat2[1][0] value: -1.3
    Enter Mat2[1][1] value: 4
    Enter Mat2[1][2] value: -2
    Resultant Matrix:
    7 -5.7 13
    5.37 13 -9






## 6) ***CRITICS***

As every coin has two faces, there are also limitations to gmat.
* limited to 2D geometric problems and visualisations.
* Unlike Python, You need to include the libraries as per requirement to ensure your code works without errors.
* gmat can handle overflow issues better than other languages, but still has its limit.
* gmat doesn't ensure taking care of memory leaks or garbage data collection.
* Giving it has properties of general purpose programming language inspired from C,C++ and specific functional programming for special purposes, gmat is not that well when it comes to mobile app development.
* cost of memory required for functinal programming may not be controlled by the user.

## 7) ***CONCLUSIONS***

Thus with the help of gmat solving plane geometry probelms, data analysis and plotting can be done easily without being compromised with general purpose programming features.

gmat allows the user to run the same program on different systems or interfaces at ease thus offering portability or platform independent features. To decrease the burden on user memory allocation is left to the compiler.

gmat helps in the development of applications/algorithms
* to solve astronomical problems
* to visualise computational geometry
* to implement Database
* to implement Spreadsheets

The syntax of this language is so handy that, a beginner can opt this language for practice. In addition to that, this language can provide a high-level understanding of the programming concepts.

###### In a nut shell gmat is a robust programming language and provides an easy usage of the code lines, maintenance can be handled in a great way, and debugging can be done easily too.

#### ***THINGS WE LEARNED FROM THE PROJECT***

* How different languages are evolved and designed with time and need.
* The importance of designing a language properly, ensuring lesser bugs.
* how new header files/libraries can be created.
* regular expressions and context-free grammars, which designers use to describe program syntax
* The scanning and parsing algorithms that a compiler or interpreter uses to recognize that syntax.
* pragmatics,external and internal linkages, and scoping of programming languages.
* group working ,team management, taking resposibilities, making decisive judgements.




## 8) ***APPENDIX A***

#### A.1.Introduction

The manual so-called describes the language 'gmat' in detail. 'gmat' is an efficient, powerful and yet easy to use programming language from general-purpose to high-level use. The focus of this reference manual is on the language itself, not the implementation of it. The language constructs are described in the text and with examples rather than formally specified. This is to make the manual more readable. While coming to the prerequisites, this manual is written assumed that the reader has a minimal idea in aspects of a programming language such as control flow, data types and object-oriented. The core of the manual consists of a series of chapters on various topics. The topics have been chosen by the complexity, importance and frequency of their use in programming.

### A.2.Lexical Conventions
Any gmat program consists of one or more translation units stored in files. It is then translated into several phases for better performance. The Initial phases of the program will do low-level lexical transformations, carry out directives(libraries) introduced by the lines beginning with the ‘add_library :+’ , and then perform macro definition and expansion. Later, the program gets to sequence of tokens after the preprocessing of (A.12) is completed.

### A.2.1 Tokens
In gmat programs, each word and punctuation is referred as a token. The compiler breaks a program into the smallest possible units and proceeds to the various stages of the compilation, which is called token. Tokens are the smallest building block or smallest unit of a program.

In gmat, there are five classes of tokens: identifiers, keywords, constants, operators, and other separators. Blanks, horizontal and vertical tabs, newlines, and comments as described below (collectively, ''white space'') are ignored except as they separate tokens.

Note: Except for horizontal tab spaces, they are used to differentiate the block of codes or scope used in the indentation are percieved by the compiler otherwise are ignored.  

#### A.2.2 Comments
A comment is an explanation of source code of the program for better understanding and readability of the user. At run-time, a comment is ignored by the compiler. There are two types of comments in gmat:

* Single-line comments, indicated by “~~comments”
* Multi-line comments, indicated by “~comments ~”

#### A.2.3 Identifiers

In gmat programming, each program element is known as an identifier. They are used for naming of variables, functions, array etc. where ever necessary.
The first character of an identifier must be an alphabet; the underscore ‘_’is also counted as a letter. Uppercase and lowercase letters are considered as different letters. Identifiers may have any length, Internal identifiers include preprocessor macro names and all other names that do not have external linkage. Identifiers with external linkage are more restricted

#### A.2.4 keywords
Keywords are predefined, reserved words in gmat and each of which is associated with specific features. These words should not be used as identifiers.
```js
_num      _string    _polygon     _poly    _conic    struct    auto     union
break     else       switch       case     typedef   return    enum     register
volatile  const      continue     for      void      default   goto     extern
sizeof    do         if           static   while     _point  
```

#### A.2.5 Constants
#### Real number constants

A real number constant consists of an integer part, a decimal part, a fraction part. The integer and fraction parts both consist of a sequence of digits. Either the integer part, or the fraction part (not both) may be missing; the decimal part may or may not be present. The type is determined by the suffix ‘_num’

#### String constants

A string consists of group of characters, which are enclosed in “ ”. The type is determined by the suffix ‘_string’

### A.3. Syntax Notation
In this manual, syntactic notation is given in the following way:

*	literal words and characters in typewriter style.
*	Programming part is highlighted in boxed structures.

#### A.4.1: Identifiers

Identifiers refer to the names of functions; classes; variables; enumeration constants and objects..etc. The Identifier's name begins with an underscore or lower/upper case letters. An identifier can't be named after a keyword.

Object or variable identifiers are defined only under their scope. Each object identifier has a region of the program where it is known(that is the scope of the object). The object gets destroyed as its scope is exited. Along with scope, Objects also have a linkage that determines whether the same name in different scope refers to the same object.
Automatic objects are local to their scope or block of code. If an object is not declared with static-specifier or if declared with auto-specifier is considered an automatic variable. Static objects storing methods are different compared to the automatic objects, this enables them to store their values even after exiting the block. The latter is declared by adding a keyword static in front of its declaration, The linkage used here would enable them to continue with their previously-stored values when the block of code is called again. static objects declared in a translational unit have internal linkage. The objects declared globally along with function declarations are always static, this gives them external linkage.

#### A.4.2: Types of Objects

The most fundamental types we have are _num and _str Types. _str type variables have a definite memory to store each character variables. _num, unlike _str, provides memory based on the value stored in the object. This ensures appropriate memory usage but there do exist limits to the range of values that can be stored in _num type variables. The io.LIB libraries also contain the ranges in MIN__num and MAX__num. In general, it provides a space as that of a single precision float point. If the input variable overflows the limits of MAX__num, the corresponding modulo value is produced.

void type specifies an empty set of values.

Constructed from these fundamental types, we also have a class of derived types like :

* arrays of objects of given types
* functions ;structures ;classes
* pointers of an object of given types
* graphs of object of given Types
* polygons; polynomials; conics of objects(arrays of expression in general) of given types

### A.4.3: Type Qualifiers

Type Qualifiers add additional information to the type of objects. There are two such Qualifiers constant(const object) and volatile(volatile object). Const objects are unmutable, trying to change them would give a runtime error or undefined behavior if you use pointers to address to change it.
Further discussion of Qualifiers is done in section_A.8.

### A.5.Objects and Lvalues

An object is simply a name for the storage allocated and Lvalue is something that refers to the name, while identifiers are names given to different entities such as classes, functions, variables. Declarations often establish a necessary mapping between objects and identifiers. For mapping identifiers and objects, we must have at least two attributes namely storage class and data type.

The range of objects that can be declared includes:
*	 variables
*	 functions
*  data types
*	 arrays, strings
*	 classes
*	 preprocessor macros

while coming to Lvalues, it is an object locator as mentioned above, an expression that designates an object. For sample example, an Lvalue expression is *ptr, where ptr here refers to any non-null pointer dealing expression. Simply a modifiable Lvalue is an identifier or expression that relates an object that can be accessed and legally changed in memory. For example, a constant pointer to a constant is not a modifiable Lvalue, since the dereferenced value cannot change. At last, if num1 and num2 are two different non-constant number identifiers with proper allocation of memory, both of them can be modified lvalues, which eventually suggests that num1 and num2 can be assigned and changed in an expression.

### A.6.1 : Pointers and Numbers
An expression of numerical type may be added to or subtracted from a pointer; in such a case the numerical expression is converted as specified in the discussion of the addition operator.

Two pointers to objects of the same type, in the same array, may be subtracted; the result is converted to an number as specified in the discussion of the subtraction operator. An numerical constant expression with value 0, or such an expression cast to type void *, may be converted, by a cast, by assignment, or by comparison, to a pointer of any type. This produces a null pointer that is equal to another null pointer of the same type, but unequal to any pointer to a function or object.

Certain other conversions involving pointers are permitted, but have implementation-defined aspects. They must be specified by an explicit type-conversion operator, or cast. A pointer may be converted to an numerical type large enough to hold it; the required size is implementation-dependent. The mapping function is also implementation-dependent.

A pointer to one type may be converted to a pointer to another type. The resulting pointer may cause addressing exceptions if the subject pointer does not refer to an object suitably aligned in storage. It is guaranteed that a pointer to an object may be converted to a pointer to an object whose type requires less or equally strict storage alignment and back again without change; the notion of "alignment" is implementation-dependent, but objects of the char types have least strict alignment requirements. A pointer may also be converted to type void * and back again without change.

A pointer may be converted to another pointer whose type is the same except for the addition or removal of qualifiers of the object type to which the pointer refers. If qualifiers are added, the new pointer is equivalent to the old except for restrictions implied by the new qualifiers. If qualifiers are removed, operations on the underlying object remain subject to the qualifiers in its actual declaration.

Finally, a pointer to a function may be converted to a pointer to another function type. Calling the function specified by the converted pointer is implementation-dependent; however, if the
converted pointer is reconverted to its original type, the result is identical to the original pointer.

## A.6.2 : Void
The (nonexistent) value of a void object may not be used in any way, and neither explicit nor implicit conversion to any non-void type may be applied. Because a void expression denotes a
nonexistent value, such an expression may be used only where the value is not required. An expression may be converted to type void by a cast. For example, a void cast documents the discarding of the value of a function call used as an expression statement.

## A.6.3 : Pointers to Void
Any pointer to an object may be converted to type void * without loss of information. If the result is converted back to the original pointer type, the original pointer is recovered. which generally require an explicit cast, pointers may be assigned to and from pointers of type void *, and may be compared with them.
This interpretation of void * pointers is new; previously, char * pointers played the role of generic pointer. The ANSI standard specifically blesses the meeting of void * pointers with object pointers in assignments and relationals, while requiring explicit casts for other pointer mixtures.

## A.7.Expressions

Expressions in 'gmat' has atleast one operand and zero or more operators, same as the other programming languages have. Operands are objects such as constants, variables, function calls and return types (data types).

	For example:
		898
		84.23 + 66.5
		tangent(56r)
		( 45 * ( 2 + 3)/ (2 - 6) )

These are all expressions in 'gmat', where in the fourth example, it is evaluated according to the predecence rules mentioned in the chapter***, while the outermost parenthesis are completely avoidable. An operator specifies an operation to be performed on its operands. operators may have one, two or three operands, depending on the operator.

## A.7.1.pointer conversion
Pointers serve a very good purpose in supporting languages,so does here. pointer have the address stored of a particular memory block. One can use address operator '&' for dereferencing a pointer to get memory address of object stored.

	For example:
		_num var = 5.5
		_num* ptr_var = &var
It's not necessary to use the dereferencing operator to obtain the address of a function. Function pointers are not compatible, in the sense we cannot expect to store the address of a function into a data type pointer, then copy into another function pointer and we can call it successfully, but its not a reliable technique in 'gmat'.
```js
_num var = 5.5, number
_num* ptr

ptr = &var ~~ the _num pointer ptr now have the memory address of var
number = *ptr ~~the value of var is copied into number
```  

Dereferencing a pointer which is not initialized may give unwanted output. So it is better to avoid dereferencing of uninitialized pointers.


## A.7.2.Primary expressions
An expression enclosed in parenthesis is called a primary expression. Simply, primary expressions are the building blocks of complex expressions. They may be string literals, variables, names qualified by the kwywords or so.

	Examples:
		100
		'c'  
		"string literal"
		operator overload '+'
		( var + 1 )
		functionfoo::

  These are all considered as primary expressions in 'gmat'.

## A.7.3.Postfix expressions

Postfix expressions consist of expressions in which postfix operators follow a primary expression. The postfix operators are listed in the following table. The operators groups from left to right.

	some of the notations:
		function call operator ::
		subscript operator []
		type-conversion operator type_name:
		member accessor in class ->(mostly) or .(also)
		postfix increment operation ++
		postfix decrement operation --

possible syntax for postfix expressions in 'gmat'

    postfix-expression[expression]
    postfix-expression(expression-list) simple-type-name(expression-list)
    postfix-expression.name
    postfix-expression->name
    postfix-expression++ 	
    postfix-expression--

#### A.7.3.1 Array references
A postfix expression followed by an expression in square brackets is a postfix expression for denoting the subscripted array reference. Either one of the two must have a pointer pointing to some data type. Subsequently suggesting that the other one must be an integer type.
```js
		let array[5] = {0,1.4,2,3.6,4}
		array[3] = 3.6
```    
where array is simply a pointer pointing to the _num data type and the integer is
present in the subscript notation. It eventually denotes that it is simply returning *(array + 3) memory block.

#### A.7.3.2 Functioncalls
Well we know, with the general notion of programming knowledge, that function is something that we need to have in our code to avoid any code duplication and for better readability. Let's have a look in 'gmat' function calls,

when a function is called, these following two things primarily happens. firstly, all actual arguements are evaluated, there is no particular order in which these arguments are evaluated, but all are evaluated and all effects are completed prior to entry in the function. secondly each formal arguement is initialized with corresponding actual arguments in the expression list. And then it executes the rest.

Example:
```js
	suppose fprime is a function which takes _num as input and gives _num as output
	_num prime = 7
	_num var = fprime:prime
```    

This is the function call syntax for functions in 'gmat'
And also there are many more inbuilt libraries for plotting and solving the geometry problems with an ease, the function calling is same though in every context.

### A.7.3.3	classes reference
This comes under the member access in the class where we need to call function or access the class members. In general the access is done with (dot). operator for normal members and (arrow)-> operator for pointer variables.

let us create a class :-
```js    
		class memberaccess
			private:
				_num privatenumber
			public:
				_num publicnumber
				_num* ptr_to_number
```
and after once they are initialized, we can access members as memberaccess.publicnumber , memberaccess->ptr_to_number another form of *(memberaccess).ptr_to_number. But the access to private members can be done only within the class without using access operators.

### A.7.3.4 Postfix incrementation/decrementation:
A postfix expression followed by double + or - operator comes under this section. It increments or decrements according to the operator given and type of the operand. If it is a number type, then it increments or decrements it by 1 or so based on the condition and if it is a pointer type, then it gives the memory address of incremented or decremented reference address.

Example:

		a++ is postfix increment expression which suggests that a = a+1
		*ptr-- is postfix decement expression which returs the previous memory block of ptr.

### A.7.4 Type Casting
casting, generally referred as type casting is used to make an expression to be a specific data type. Type cast in 'gmat' generally consists of datatype followed by colon. Also casting is allowed only to the scalar types, like number type, string literal or a pointer type.

	cast-expression = (type_name)tobe_castedexpression
	Example:
		_num var = 10
		_str string = _str:var
		now string contains a string literal "10"
		similary a pointer from one datatype to other datatype also can be successfully casted in 'gmat'.

## A.7.5 Multiplicative operators
The multiplicative operators *,/ and % functions from left to right.
The operands of * and / must have arithmetic type, generally takes any numerical value except the '0' for division, while % operand must have integral type. _num make sures all are used correctly whenever necessary. And these follows standard rules of mathematics while solving the operations. However, we can load these operators too.

## A.7.6 Additive operators
The additive operators + and - also functions from left to right. If the operands are of numerical type, usual arithmetic operations are performed. These operators also wrok on pointers. Same as the arithmetic operations these serve the purpose of pointer arithmetic where we can get the incremented or decremented memory address as we fill the instruction.

## A.7.7 Shift operators
The shift operators << and >> both must have integers as arguments in the expression if these are considered as functions, as operands if considered as operators. Generally we use left shift operator << to shift first operands bits to the left, the second operator denotes the number of bit places to shift. similarly we use the right shift operator >> to shift the first operands bits to the right. Bits which shifts out gets discarded and added are generally 0. If Negative or value greater than bitwidth is used as second operand, it would give unwanted results.

## A.7.8 Relational operators
The relative operators have left to right associativity. Both operators must be of arithmetic or pointer type.

	operators:
		less than <
		greater than >
		less than or equal to <=
		greater than or equal to >=

It comes with a bit tricky in terms of using these operators on pointers. If two pointers point to elements of the same array or to element beyond the array, the pointer object with higher subscript is treated higher. If class type is union, then pointers to different data members in the same union are treated equal. And also these operators are to be used only when pointers are of same type.

## A.7.9 Equality operators
The two most used operators == and != are coined under equality operators because of the work they do. == is equality operator and != is not equal operator.
If both the operands are equal then == returns true and != returns false and vice versa.

## A.7.10 Bitwise AND operator
The bitwise AND operator '&' compares each bit of first operand to each bit of the second operand. As it does from standards, if both the bits are 1 then the resultant bit is 1 and subsequently all the other leads the resultant bit to be 0. Both the operands for this operator must be integers.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 & var2

## A.7.11 Bitwise OR operator
### A.7.11.1 Exclusive
The bitwise exclusive OR operator ^ compares each bit of first operand and corresponding bit of second operand. If the bits of either one of the operand is 1 then resultant bit is 1 and else the resultant bit is set to zero. Both the operands must have iteger type.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 ^ var2

### A.7.11.2 Inclusive
The bitwise inclusive OR operator | compares each bit of its first operand to corresponding bit of second operand. If either bit is 1 , resultant bit is set to 1 , else bit is set to 0. Also both the operands must have integer type.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 | var2

## A.7.12 Logical AND operator
The logical and operator && returs 1 if both operands are 1 and else results in 0. The operands doesn't need to be of same type. They have left to right associativity. This operator is confined to boolean, number or pointer type.

## A.7.13 Logical OR operator
The logical or operator || returns 1 if either one of the operands are 1 and else results in 0. Similarly this operand doesn't need to be of same type. It's left to right associative. This operator is also confined to boolean, number or pointer type.

## A.7.14 Conditional operators
The conditional operator is a ternary operator ()?():() The first operand here is converted to integer 1 or 0. If first operator is 1 then second operand is set to evaluated else the third operand is set to evaluated. Which suggests that only one of second or third operand is evaluated. It have right to left associativity.

	For example:
	_num i = 10.5 , j = 27.33
	write(i>j?i:j,"is greater than the other")

## A.7.15 Assignement operators
The assignment operators store a value in the object specified by the left operand. simple and compound assignments divide these operators. Simple assignment is the one which the value of second operand is stored in the object of first operand. Where the compund assignment is performed without storing.

		= storing the value
		*= multiply the firstoperand to second and stored in first
		/= divide the firstoperand to second and stored in first
	 	%= gives the modulus of first operand and is stored in first
	 	+= adds the first operand , sceond operand and is stored in first
	 	-= substracts the first operand , sceond operand and is stored in first
	 	<<== leftshifts the operand by the value and hets stored in first operand
	 	>>== rightshifts the operand by the value and hets stored in first operand
	 	&= stores the bitwise and of two operands in first operand
	 	^= stores the bitwise exclusive or of two operands in first operand.
	 	|= stores the bitwise inclusive or of two operands in first operand.
```js    
	Example
		_num a = 1 , b = 2 , c = 3 , d = 4
		a += b
		b -= c
		c *= d
		d /= c
		c %= d
		a |= d
		these all comes under assignment operators.
```		
## A.7.16 Comma operator
The two operands seperated by comma gets evaluated left to right. Commas can be used as separators in function araguments and function calling.

	_num var1 = 10.5 , var2 = 0.23 , var3 = 666
	var1 = var2,var3
	write(var1)
	var1 = (var2,var3)
	write(var1)

It yields different results.

## A.7.17 Constant expressions
Constant expressions are the ones which are not subjected to change. If we are supposed to have a data literal which shouldn’t change its value or contents at any point of time in execution of program, this constant expressions are made for you.

    Example:
    const _num variable = 10
    this variable never changes with course of time.
    Similarly const can be used before any data type. Contents in const type remains intact.

## A.8 Declarations
Declarations specify the interpretation given to each identifier; they do not necessarily reserve storage associated with the identifier.  A declaration must have at least one declarator, or its type specifier must declare a structure tag, a union tag, or the members of an enumeration; empty declarations are not permitted (Declarators will be discussed later (Par.A.8.4); they contain the names being declared)

Declarations have the form declaration:
“declaration-specifiers declarator-list”
* The declarators in the declarator-list contain the identifiers being declared.
*  The declaration-specifiers consist of a sequence of type and storage class specifiers.

## A.8.1 Specifiers

### i) Storage Class Specifiers
#### 1) auto
The auto specifiers may be used inside the functions and give the objects (which are declared) automatic storage class, and these type of declarations serve as definitions and cause storage to be reserved
#### 2) register
A register declaration is equivalent to an auto declaration, but now, the declared objects will be accessed more frequently. only certain types are eligible; the restrictions are based on implementation. However, if an object is declared register, the unary ‘&’ operator may not be applied to it, explicitly or implicitly.
#### 3) static
The static specifier gives the object which are declared, static storage class, and can be used either inside or outside functions. This specifier causes storage to be allocated inside the function, and serves as a definition; for its effect outside a function.
#### 4) extern
The extern specifier specifies that the storage for the declared objects is defined elsewhere; for its effects outside a function.
#### 5) typedef
The typedef specifier does not reserve storage and is called a storage class specifier only for syntactic convenience  

At most one storage class specifier may be given in a declaration. If none is given, these rules are used: objects declared inside a function are taken to be auto; functions declared within a function are taken to be extern; objects and functions declared outside a function are taken to be static, with external linkage.

### ii) Type Specifiers
The type-specifiers are:
  *   void
  *   _num
  *   _string
  *   _point
  *   _polygon
  *   _poly
  *   _conic
  *   struct-or-union-specifier
  *   enum-specifier
  *   typedef-name  

Types may also be qualified, to indicate special properties of the objects being declared.

type-qualifier:
  *  const
  *  volatile

Type qualifiers may appear with any type specifier.
 A const object may be initialized, but not thereafter assigned to.
There are no implementation-dependent semantics for volatile objects.

## A.8.2 Structure and Union Declarations
A structure is an object consisting of a sequence of named members of various types. A union is an object that contains, at different times, any of several members of various types.

Structure and union specifiers have the same form.
A struct has a declaration list, which is a sequence of declarations for the members of the structure or union:

    Example:
      struct Address
	       _num street_No
	       _string street_Name           ~This the declaration list of struct Address~
	       _string city
           struct Address*next

           ~It contains street number, name of the street, name of the city ~
      struct Address k
      struct Address *p
           ~declares k to be a structure of the given sort, and p to be a pointer to a structure of the given sort. ~
      p->street_No
           ~~refers to the ‘street_No’ field of the structure to which p points;
      k.next
           ~~refers to the next pointer of the structure k.

## A.8.3 Enumerations
 Enumerations are unique types with values ranging over a set of named constants called enumerators.

The identifiers in an enumerator list are declared as constants of type _num, and may appear wherever constants are required. If no enumerations with = appear, then the values of the corresponding constants begin at 0 and as the declaration is read from left to right, each constant increase by 1. An enumerator with = gives the associated identifier the value specified; subsequent identifiers continue the progression from the assigned value.

    Example:
    add_library :+ io.LIB
    enum Month{Jan, Feb, Mar, Apr}   ~~Jan=0,Feb=1,Mar=2,Apr=3
    main::_num
	    enum Month x
        x=Mar
        write(x)
        return 0

        OUTPUT: 2
Importantly, Enumerator names must all be distinct from each other and from ordinary variable names, but the values need not be distinct.

## A.8.4 Declarators
A list of declarators appears after a sequence of type and storage class specifiers. Each declarator declares a unique main identifier. The storage class specifiers apply directly to this identifier, but its type depends on the form of its declarator. (see below pointer, array declarators)

#### i)pointer declarators
The declaration of pointer has the following syntax:
“Datatype * identifier”

For example, consider the declaration

_num *ap

Here, ap plays the role of an identifier; the declaration ''_num ap'' would give ap the type '' _num'', but now the actual declaration “_num *ap” gives ap the type `` pointers to _num''

#### ii) array declarators
The declaration of an array has the following syntax:
“Datatype identifier[constant-expression]”

If the constant-expression is present, it must have integral type, and value greater than 0. If the constant expression specifying the bound is missing, the array has an incomplete type.

An array may be constructed from an arithmetic type, from a pointer, from a structure or union, or from another array (to generate a multi-dimensional array)

    Example:
    _num a1[17], *a2[17] ~declares an array of real numbers, an array of pointers to real(_num)   

#### iii) function declarators
In gmat, a function declaration has the syntax of the form:
“FunctionName(identifier) : parameters-list : return-type ;”

The parameter-list specifies the types of the parameters. For a function with no parameters has an empty parameter-list and with return type “void”.

    Example:
    strcpy : _num *dest,  _string source : _num
    ~strcpy is a function returning ‘_num’, with two arguments, the first one is ‘_num’ pointer, second one is a string. ~

## A.8.5 Initialization
When an object is declared, then its declarator may specify an initial value for the identifier being declared.

The initializer is preceded by =, and is either an expression, or a list of initializers nested in braces.

    Example: _num x = 3

#### i)array initialization
For an array, the initializer is a brace-enclosed list of initializers for its members (as shown in the example below). If the array has unknown size, the number of initializers determines the size of the array, and its type becomes complete.
Example: _num x[] = {1,2,3}
If the array has fixed size, the number of initializers may not exceed the number of members of the array; if there are fewer, the trailing members are initialized with 0.  The number of initializers must not be greater than the number of elements to be initialized.

    Example: _num y[3] = {1} ~~array with fixed size
                        ~~only, y[0] is initialised to ‘1’ , and others i.e, y[1],y[2] are initialized to ‘0’
#### ii)pointer or arithmetic type
The initializer for a pointer or an object of arithmetic type is a single expression. The expression is assigned to the object.
That is, to assign a value to an arithmetic or pointer type, use the simple initializer: = expression.

    Example: _num x= 3, _num *p=&x  
#### iii)_point datatype
There are two initializers for a _point datatype enclosed by “[“,”]” this set of brackets as shown below.

    Example: _point P = [-2,3]

#### iv)_polygon datatype
Number of initialisers for _polygon datatype depends on the number of sides of the polygon required.
These initialisers are separated “;” and all are enclosed by “[“,”]” this set of brackets, as shown below.

    Example: _point A= [0,0], B= [0,4], C= [3,0]
                  _polygon Tri = [A; B; C] ~~Tri is a right-angled triangle
#### v)_poly datatype
Number of initialisers for _poly datatype depends on the degree of the polynomial required.
These initialisers are separated “,” and all are enclosed by ‘[‘  , ‘]’ this set of brackets, as shown below.

    Example: _poly Eqn=[1,2,3]
    ~~ The initialisers are coefficients ‘x^n’ in decreasing order of power of x
    ~~Eqn represents the polynomial:  1*x^2 + 2*x + 3


#### vi)_conic datatype
There are six initializers for a _conic datatype enclosed by “(“,”)” this set of brackets and each each initialiser is separated by ‘, ’, and finally, initialising a conic with the help of ‘inject’ function as shown below.

    Example: _conic var.inject(1,0,1,0,0,-9)
      ~conics general equation ax^2+2hxy+by^2+2gx+2fy+c~
      ~Here var is a circle with centre origin and radius 3 ~
#### vii)_string datatype
The initializer for _string datatype is group of characters enclosed by “ ”, as shown below.

    Example: _string Name= “Principles of Programming Language-1”
#### viii)structure or union
The initializer for a structure is either an expression of the same type, or a brace-enclosed list of initializers for its members in order. Unnamed bit-field members are ignored, and are not initialized. If there are fewer initializers in the list than members of the structure, the trailing members are initialized with 0. There may not be more initializers than members.

    Example:
      struct address
	       _num street_No
	       _string street_Name
	       _string city
      struct address My_address= {“12”,” Kandi”,” Hyderabad”}
#### A.8.6 Typedef

Declarations whose storage class specifier is typedef do not declare objects; instead they define identifiers that name types. These identifiers are called typedef names.
A typedef declaration attributes a type to each name among its declarators in the usual way . Thereafter, each such typedef name is syntactically equivalent to a type specifier keyword for the associated type.
A typedef does not introduce new types, only synonyms for types that could be specified in another way.

    Example:
    typedef _num Block
    ~~after the above declaration
    Block b   ~~ It is a legal declaration. The data type of b is _num

## A.9 : Statements

Statements are executed in sequence. Statements are executed for their effect, and do not have values. They fall into several groups.

```js
  statement:
    labeled-statement
    expression-statement
    compound-statement
    selection-statement
    iteration-statement
    jump-statement
```

## A.9.1 : Labeled Statements

Statements may carry label prefixes.
```js
  labeled-statement:
    identifier : statement
    case : constant-expression : statement
    default : statement
```
A label comprising of an identifier declares the identifier. The only use of an identifier label is as a target of "jump". The scope of the identifier is the current function. Since labels have their own name space, they don't meddled with other identifiers and cannot be redeclared. Case names and default labels are utilized with the switch statement. The consistent expression of case must have "numerical type" or "string type". Labels themselves do not alter the flow of control.

## A.9.2 : Expression Statement

expression Statement are in the form
```js
  expression-statement:
    expression
```
Most expression statements are assignments or function calls. All side effects from the expression are completed before the next statement is executed. If the expression is missing, the construction is called a null statement; it is often used to supply an empty body to an iteration statement to place a label.

## A.9.3 : Compound Statement

So that several statements can be used where one is expected, the compound statement (also called "block") is provided. The body of a function definition is a compound statement.
```js
  compound-statement:
    declaration-listopt statement-listopt
  declaration-list:
    declaration
    declaration-list declaration
  statement-list:
    statement
    statement-list statement
```
If an identifier in the declaration-list was in scope outside the block, the outer declaration is suspended within the block, after which it resumes its force. An identifier may be declared only once in the same block. These rules apply to identifiers in the same name space; identifiers in different name spaces are treated as distinct.

Initialization of automatic objects is performed each time the block is entered at the top, and proceeds in the order of the declarators. If a jump into the block is executed, these initializations are not performed. Initialization of static objects are performed only once, before the program begins execution.

## A.9.4 : Selection Statements

Selection statements choose one of several flows of control.
```js
  selection-statement:
   1) if: expression
      statement
   2) if: expression
      statement
      else:
      statement
   3)switch : expression
      statement
```
In both forms of the "if" statement, the expression, which must have arithmetic or pointer type, is evaluated, including all side effects, and if it compares unequal to 0, the first substatement is executed. In the second form, the second substatement is executed if the expression is 0. The "else" ambiguity is resolved by connecting an "else" with the last encountered "else"-less "if" at the same block nesting level.

The "switch" statement causes control to be transferred to one of several statements depending on the value of an expression, which must have "Numerical type" or "string type". The substatement controlled by a "switch" is typically compound. Any statement within the substatement may be labeled with one or more "case" labels. The controlling expression undergoes "numerical or string" promotion, and the case constants are converted to the promoted type. No two of these case constants associated with the same switch may have the same value after conversion. There may also be at most one "default" label associated with a switch. Switches may be nested; a "case" or "default" label is associated with the smallest switch that contains it.

When the "switch" statement is executed, its expression is evaluated, including all side effects, and compared with each case constant. If one of the case constants is equal to the value of the expression, control passes to the statement of the matched "case" label. If no case constant matches the expression, and if there is a "default" label, control passes to the labeled statement.If no case matches, and if there is no "default", then none of the substatements of the swtich is executed. The controlling expression of switch, and the case constants, were required to have "_num type or _str type".

## A.9.5 : Iteration Statements

Iteration statements specify looping.
```js
  iteration-statement:
    1)while: expression
      statement
    2)do
        statement
      while: expression
    3)for:expression1, expression2: expression3:
       statement
```
In the "while and do statements", the substatement is executed repeatedly so long as the value of the expression remains unequal to 0; the expression must have arithmetic or pointer type. With "while", the test, including all side effects from the expression, occurs before each execution of the statement; with do, the test follows each iteration.

In the "for" statement, the first expression is evaluated once, and thus specifies initialization "for" the loop. There is no restriction on its type. The second expression is evaluated after each iteration, and thus specifies a re-initialization "for" the loop. The third expression must have arithmetic or pointer type; it is evaluated before each iteration, and if it becomes equal to 0, the for is terminated.There is no restriction on its type. Side-effects from each expression are completed immediately after its evaluation. If the substatement does not contain continue,a statement
```js
  for: expression1, expression2: expression3:
    statement
is equivalent to
expression1
while: expression3
statement
expression2
```
Any of the three expressions may be dropped. A missing third expression makes the implied test equivalent to testing a non-zero element.

## A.9.6 : Jump statements

Jump statements transfer control unconditionally.
```js
  jump-statement:
    jump identifier
    continue
    break
    return expression
```
In the "jump" statement, the identifier must be a label located in the current function.
Control transfers to the labeled statement.
A continue statement may appear only within an iteration statement. It causes control to pass to the loop-continuation portion of the smallest enclosing such statement. More precisely, within each of the statements
```js
  1)while:....
      .......
      continue
  2)do:....
      .......
      continue
    while:....
  3)for:.....
      .......
      continue
```
a "continue" not contained in a smaller iteration statement is the same as jump continue.

A "break" statement may appear only in an iteration statement or a "switch" statement, and terminates execution of the smallest enclosing such statement; control passes to the statement following the terminated statement.

A function returns to its caller by the "return" statement. When "return" is followed by an expressions, the values is returned to the caller of the function. The expressions is converted, as by assignment, to the type returned by the function in which it appears. There can be two or more return expressions. Flowing off the end of a function is equivalent to a return with no expression. In either case, the returned value is undefined.

```js
function:argumnets:return_1,return_2
    function body
    return x,y
  ~~x,y contain the values to be returned.
  ~~x,y correspond to return_1 and return_2 respectively

main::_num
    _num a,b
    (a,b) = function:arguments:

```

## A.10

The input to the compiler is provided in units(called translational/computational units), each consisting of a sequence of external declarations/ function definitions. These units form the final input to the compiler from which object files are generated. The scope of the external declaration lies till the end of the unit.

```js
  computational unit:
    external declaration:
      function defination
      declarations ...
      computational units:external declarations ...
```

Simply put declaring an object outside of a function is called an external declaration. (the object is declared without being defined). Note that memory allocation is done while defining the object.

## A.10.1 : Function Definations

In gmat function definition format is like this:

The functions Declarater consists of the function identifier and the arguments declaration specifiers and their idenatifiers respectively.
```js
func_identifier:arg_declaration_specifier arg_identifier:func_declarater_specifier
     code of the function program

```
multiple arguments can be provided separated by commas, and similarly, multiple declaration specifiers can be given, an indication that function would return more than one value/object.

A function may return an arithmetic type, a structure, a union, a void, but never an array or another function pointer. The parameters list is the arguments lists along with their declaration specifiers, The parameter list refers to the type, order, and the number of parameters in the function. If no declaration is given for the parameter it is taken to be of _num type. Default parameter initialization is allowed in CPP, it is better to write them at the end of the parameter list.

Note: Functions won't be able to return arrays, but the Solve: Equation functions are defined in the geo.LIB function has the ability to store the final result in an array directly. The type of implementation used here is inspired by lists used in python.

## A.10.2: External Declarations

External declarations are used to specify the characteristics of objects, functions, and other identifiers. External declarations discuss the declaration of functions/objects; it's different from the keyword 'extern'.

External Declarations format/syntax :
```js
func_identifier:arg_declaration_specifier arg_identifier:func_declarater_specifier;
```
Different external declarations may exist for the same identifier only if they agree in both type and linkages, and there should be only one definition for the identifier.
```js
static _num x=2  ~~definition; internal linkage
_num x           ~~tenative definition: gives undefined behavior
                 ~~     since there should be only one definition for an identifier
```
If an external object declaration does not contain an 'extern' specifier then it's called a tentative definition. if no further definition for the object appears then the tentative definitions initialize objects to zero or else they just become redundant declarations. If the static specifier is not used in the object's first declaration then the object is considered under external linkage.
```js
_num x = 10        ~~definition; external linkage  
_num x             ~~tentative definition; becomees a redundant declaration here
extern _num x      ~~extrnal declaration; refers to the earlier defination

_num y             ~~tentative definition; intialised to 0
static _num p      ~~tentaive definition; internal linkage
_num q             ~~external declaration; external linkage

_num z             ~~tentative definition; becomes redundant declaration here
extern _num z =10  ~~external definition
```
```js
static _num x
extern _num x=6  
~~ doesn't throw an error(x gets initialized and declared as extern) but once the extern is defined inside a function it throws an error

static _num y=5
extern _num y
~~ here y is initialized and declared as static and the second line becomes redundant.

static _num z=6
extern _num z=5
~~ throws an error
```
objects with the internal linkage must have the same definitions in its translational unit since they are internally linked objects. objects with the external linkage must have the same definition through out the program.

## A.11

A program need not all be compiled at one time: the source text may be kept in several files containing translation units, and precompiled routines may be loaded from libraries. Communication among the functions of a program may be carried out both through calls and through manipulation of external data.
There are two kinds of scope: first, lexical scope of an identifier which identifier's characteristics are unterstood. second, scope associated with objects and functions which determines the connections between identifiers in compiled translation units.

## A.11.1 : Lexical Scope

The lexical scope of a declaration is the declared name’s range of visibility within its own translation unit.  It begins at the end of the declaration and continues unbroken until an end point that depends on the type of declaration.  For an internal declaration, that point is the end of the containing block.  For a parameter of a function definition, that point is the end of the function.  For an external declaration, that point is the end of the translation unit.  Nested declarations of the same name have overlapping lexical scopes, and each one hides the others that are outside its own block.  A declaration of an object, including the extern keyword, which occurs earlier than the object’s definition in the same source file, commences the lexical scope at the earlier point.

All function definitions are external, since gmat does not allow nested functions.  Therefore, a translation unit consists of external declarations (declarations of objects and functions) and function definitions.

## A.11.2 : linkage

gmat can (and often is) implemented to use different linkage conventions. The most basic reason for that is gmat’s greater emphasis on type checking. A practical reason is that gmats supports overloading, To begin with external decleration for an identifier gives the identifier internal linkage in the event that the "static" specifier is utilized, external linkage otherwise. If a decleration for an identifier inside a block does not incorporate the "extern" specifier, at that point the identifier has no linkage and is one of a kind to the function . In case it does incorporate "extern", and an external statement for is dynamic within the scope encompassing the piece, at that point the identifier has the same linkage as the exernal decleration, and refers to the same object or function; but in case no external decleration is visible, its linkage is external.


## A.12.Preprocessing

Preprocessors ensure that the code is preprocessed(inclusion of files, symbolic preprocessing of equations and conics if required, macro substitution, and conditional compilation) before the compilation starts. The preprocessor directives tell the preprocessor what to do. In gmat preprocessor directives are identified by their names, there is no '#' added at the beginning. add_library, define, ifndef, endif are some of the preprocessor directives in gmat.

## A.12.1: Digraphs and Trigraphs:

Both Digraphs and Trigraphs are omitted in gmat programming implementation. You may enable them by writing separate command lines.
```js
enable:+digraphs
enable:+trigraphs
```
When the above command lines are used compiler replaces the trigraph sequence with the corresponding punctuation character.
```js
Trigraph character     Equivalent             Digraph character   Equivalent
??=                     #                     <:                  [
??/                     \                     :>                  ]
??'                      ^                     <%                  {
??(                     [                     >%                  }
??)                     ]                     %:                  #
??!                     |                     :%                  ##
??<                     {
??>                     }
??-                     $
```
Note: A digraph string or a trigraph string occurring inside a quoted string or character constant shall not be replaced. gmat also poses additional tokens which can be accessed by default. The Trigraphs, Digraphs, and tokens (if present) are converted before the tokenization(refer to A.12.3) begins.

## A.12.2: Macro Definition and Expansion
```js
define identifier(identifier_list) token_sequence

undef identifier  ~~removes the token_sequence(if any) applied to the identifier(if any).
```
A Macro definition consists of a preprocessor directive, an identifier, and the identifier list(optional), and a token-sequence. The identifier list consists of parameters. Wherever the identifier is written, it is replaced by the corresponding token sequence. The parameters list if present is replaced by corresponding arguments in order. If the arguments list doesn't match with the parameters list it throws an error. Multiple Macro definitions for the same identifier throw an error unless they are identical. The token sequence must be written there itself, following the same indentation rules as general codes do.

example:
```js
define list_printer(start,end) while:start<end
                                   write(start," ")
                                   start++
~~ code ...

undef list_printer
```

The operation of Macro differs in presence of two operators # and ##. if a # character occurs then the identifier is replaced by the token-sequence placed inside quotes, and each " and \\ that appear are added with a \\.

## A.12.3: File inclusion

```js
add_library :+ "filename"    
add_library :+ filename      
```
Both the above command lines include the contents of the file identified by the filename into the present source file. If there is no file with the given filename then the program throws an error. The filenames used in the above command lines must not contain characters such as *,',",/,\\,'

The first command-line searches for the files under standard gmat directories. The standard gmat directories can be controlled by the user. The second command line first searches the directory where the current source file exists, and only if the file is not found, it searches through standard directories

## A.12.4: Conditional Compilation

The conditional compilation works similar to an if else-if conditions.
```js
If: expression
Ifdef: identifier
Ifndef: identifier

Elif: expression

Else:

Endif
```
The conditional processing starts with an If: or Ifdef: or Ifndef and is evaluated in order until a non-zero value is found. Only the text following the successful derivative is executed. If no non-zero value is found, the text under Else: is executed. If the identifier is defined as a macro, the macro substitution is done first. The conditional Compilation block is ended by an Endif

## A.12.5: Line control
```js
Line constant "filename"
Line constant
```
makes the compiler to believe that the next source line is given by the integer "constant" written just after the Line derivative. Macros in the line are expanded before it is interpreted.

example:
```js
write(__LINE__," ")
Line 10
write(__LINE__)
```
OUTPUT: 1 10

## A.12.6 Error Generation
```js
Error token-sequence
```
causes the preprocessor to write a diagnostic message that includes token-sequence.
* The functions related to geo.LIB may not return messages here unless the input given doesn't match with the syntax or the input is undefined, These functions are written in functional programming essence, these can't be accessed by the user. Any return of undefined values of these functions is stored as 'nan'(not a number).

## A.12.7: Pragmas
```js
Pragma token_sequence
```
The Pragma directives are used to provide some extra information. If a pragma is not identified, it is ignored.

examples:
```js
Pragma startup token_sequence
~~ before the start of main, the token_sequence is to be executed

Pragma exit token_sequence
~~ before the end of the program, the token sequence is executed
```
## A.12.8 Predefined Macro Names
```js
__DATE__  ~~ contains the date of compilation of source file in string literal form: "mm dd yyyy"
__FILE__  ~~ name of the current source file
__LINE__  ~~ The current line number
__TIME__  ~~ contains the time of compilation in the format: "hh mm ss"
```
Several identifiers are predefined. They can't be redefined again.
