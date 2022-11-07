##  ***Example 3***

* Arthimetics operators:  +,-,*,/,%

```js
add_library :+ io.LIB 

main::


    ~~precedence order is same as in all languages
    ~~ parsing is done from left to right 

    _num x=0,y=0
    _str a

    ~arithmetic operations can not be done for characters~
    x = a+b*5/2*8%2
    y = 3+4/2*5+8%3

    write(x," ",y)

    return 0
```

* OUTPUT:
line:18:error:x = a+b*5/2*8%2 : (invalid datatypes used)

line:18:error:x = a+b*5/2*8%2 : (variable b not defined)

