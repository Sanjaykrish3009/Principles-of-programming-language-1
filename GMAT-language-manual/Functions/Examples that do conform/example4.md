## ***Example 4***

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

