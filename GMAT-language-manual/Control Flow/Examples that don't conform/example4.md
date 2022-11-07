##  ***Example 4***

* jump(goto)

```js
add_library : + io.LIB 

main::_num
  
    ~degree should always be given for the datatype _poly~
    _poly Eqn
    _num x,y

    Eqn = [a,b,c]

    ~missing semi-colon(;)~
    Label
    
    write("Enter the coefficients of the equation:")
    read(a,b,c)

    (x,y) = Solve(Eqn) 
    ~the number of digits to be printed after the decimal should always be enclosed in brackets~
    write("Roots:",0.3x,",",(0.3)y)
    

    if: x==y
        write("Roots are equal\n")
    else:
        write("Roots are not equal\n") 
        jump Label         
    
    return 0
```

* OUTPUT:
line:6:error:add_library : + io.LIB : (there should be no space between : and +) 

line:11:error: _poly Eqn : ( degree was not mentioned ) 

line:16:error: Label : ( missing a semi-colon )

line:24:error: write("Roots:",0.3x,",",(0.3)y) : (error expected in "0.3x")
