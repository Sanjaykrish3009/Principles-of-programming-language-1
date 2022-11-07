##  ***Example 4***

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
