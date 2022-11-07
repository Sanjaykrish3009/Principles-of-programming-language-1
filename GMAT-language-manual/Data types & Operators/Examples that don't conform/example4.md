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
     
    ~range of a variable should always be mentioned in "VARIABLE@(range of the variable)" format~ 
    ~here the format is wrong~
    else if: y < variable <= z
    write(variable,"lies in the interval (",y," ,",z,"]","\n")

    else
    write(variable,"is greater than ",z,"\n")

    return0
```

* OUTPUT:

line:27:error: else if: y < variable <= z : (incorrect format)
