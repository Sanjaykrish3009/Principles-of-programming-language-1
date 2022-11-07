## ***Example 2***

```js
add_library :+ io.LIB

main :: _num
    write("enter a number n:")
  ~~ reads the value of n
    read(n)
  ~~ prints the square of the number(n)
    write("the square of the number ",n," is:",n*n,"\n");

    _str s
    write("enter a string:")
    for:_num(i=0),i++:i<n:
         write(s,"\n")
```




OUTPUT:

line:9:error: read(n) : (variable n was not mentioned)

line:11:error: write("the square of the number ",n," is:",n*n,"\n"); : (remove semicolon(;))

line:16:error:write(s,"\n")        : (string s was not read)
