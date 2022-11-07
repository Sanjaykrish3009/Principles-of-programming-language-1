## ***Example 2***

* functions - help in breaking large programs into smaller tasks

```js
add_library :+ io.LIB 
add_library :+ geo.LIB 

func:_str expression,_num degree:_num roots[] 
    _poly Eq:degree
    Eq =[expression]
return Eq

main::_num
    write("Enter the degree of equation :")
    _num n 
    read(n>-1)
    _str expression 
    write("Enter the coefficients in order:")
    _num final_roots[n]
    strcpy:final_roots,func:expression,n
    
    for:_num i=0,i<n:i++
        write(final_roots[0]," ")
retun 0    
```

~~functions syntax ==> function_name:arguments:return_types



