## ***Example 1***

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
