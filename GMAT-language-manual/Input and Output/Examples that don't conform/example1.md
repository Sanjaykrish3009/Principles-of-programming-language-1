## ***Example 1***

```js
add_library :+ io.LIB

~~only for printing

main :: _num

        _num x = 10
        write(x,"\n")

        _str s = "this is a string"
    ~expected comma(,)~
        write(s"\n")

    _poly Eqn:2
    _num x,y
    ~~ equation with degree 2: a*x*x + b*x + c
    Eqn = [a,b,c]
        a = 1 , b = 5 , c = 6

        (x,y) = Solve(Eqn)
    ~~ prints the roots of the equation x,y
    write("Roots:",x,",",y)

      return 0
```



OUTPUT:
line:15:error:write(s"\n") : (, expected before ")
