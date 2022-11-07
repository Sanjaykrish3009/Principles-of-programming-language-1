## ***Example 3***

```js
add_library :+ io.LIB 


redirect : : _num
    _num rand = gmat.random::
    return rand

redirect :: _str
    _str rand = "somerandomstring__"
    return rand

main::_num

    _num number
    number = redirect:

    _str s 
    s = redirect:
```


~~the following program in gmat would lead to an error , this is where the function overload fails in gmat, i.e the functions which only differ in return type. Here the functions doesn't take any input but return different outputs with different return types.





