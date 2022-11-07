##  ***Example 1***

* Scope of variables
The scope of a name is the part of the program within which the name can be used

```js

main::_num    
    _num x
    read(x)
  
    for:_num i=0,i<x:i++
        _num y+=i

    write(y," ",i)
```

~~ The scope of variable 'i' is only within the for-loop 
~~ When a variable is called/to be written the compiler searches for the variable name in the present scope first, if not present it searches if there are any in the external scope. And the variable is destroyed once the part o program(its scope) execution is done.

