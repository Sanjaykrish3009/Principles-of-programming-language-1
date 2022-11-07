## ***Example 4***

```js
add_library :+ io.LIB 

main::_num
    _num x=5
    static _num cr = x+1

    for:x,x<10:x++
        write(x," ")
    write("\n")    
    write(x,"\n")
    write(cr)
```

~~ static variables and external variables must be initialised by constants
~~ the output of for-loop would be 5 6 7 8 9 
~~and the final x value will be 9 not 5






