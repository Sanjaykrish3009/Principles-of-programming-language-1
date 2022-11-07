##  ***Example 5***

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






