## ***Example 3***

```js
add_library :+ io.LIB

main::_num
    _num n
    write("enter a number n:")
  ~~ reads the value of n
    read(n)
  ~~ prints the square of the number(n)
    write("the square of the number ",n," is:",n*n,"\n")
  
    _str s
    write("enter a string:")
  read(s)
    for:_num(i=0),i++:i<n:
        write(s,"\n")

return 0
```


OUTPUT:

enter a number n:5

the square of the number 5 is:25

enter a string:This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

This is GMAT language!!!

