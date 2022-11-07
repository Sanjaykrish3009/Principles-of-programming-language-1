##  ***Example 1***

* Variable Naming and declarations

```js
add_library :+ io.LIB 

~Variable Naming and declarations~

main::_num
    ~~ variables names can contain letters and digits.
    ~~ Gmat is case sensitive . 

    _num variable 12 = 12     ~~ variable should not contain any spaces between them
    _num 1number = 15         ~~ variable should not start with a number, it will always starts with a alphabet
    _num _var = 20            ~~ variable should not start with an underscore

    _num GMAT

    ~~ assigning of variable can be done while declaration also
  
    write(variable 12+1number+_var)


    return 0
```

* OUTPUT

line:14:error : _num variable 12; : (invalid variable name)

line:15:error : _num 1number : (invalid variable name)

line:16:error : _num  _var : (invalid variable name)

line:22:error : write(variable 12+1number+_var) : (variables are not defined properly)

line:18:warning : _num GMAT : (variable defined but not used)


