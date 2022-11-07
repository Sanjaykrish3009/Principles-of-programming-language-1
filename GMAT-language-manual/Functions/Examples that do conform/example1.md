##  ***Example 1***

* Scope of variables
The scope of a name is the part of the program within which the name can be used


```js
add_library :+ io.LIB

main::_num
    _num x
    read(x)
    _num y,i

    for:i=0,i++:i<x
        y+=i
        _num y = i+1
        write(y," ")   ~~Its first preference would be the local variable

    write("\n")    
    write(y," ",i)     
~~the "y"-variables here prints the value stored in the 'y' outside the forloop
    return 0
```
INPUT: 

5

OUTPUT:

1 2 3 4 5

10 5



