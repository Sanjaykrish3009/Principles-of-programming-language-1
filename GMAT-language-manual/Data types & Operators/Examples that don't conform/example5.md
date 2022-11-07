##  ***Example 5***

* bitwise operators , assignment operators , increment and decrementers

```js
add_library :+ io.LIB

main::_num

  _num x = 7
  _num y = 9

  _num z = x ^ y            ~~bitwise xor
  write(z,"\n")

  z = x & y                        ~~bitwise and
  write(z,"\n")

  z = x | y                        ~~bitwise or
  write(z,"\n")

  ~leftshift is always "<<" ~
  z = x < y                    ~~leftshift
  write(z,"\n")

  ~rightshift is always "<<" ~
  z = x > y                    ~~rightshift
  write(z,"\n")

  z = $x                            ~~negation
  write(z,"\n")

  ~in general expr1 op= expr2 demonstrates expr1 = (expr1) op (expr2) works for only arithmetic operators~
  x&&y
  write(x,"\n");

  return 0
```

* OUTPUT:

line:23:error: z = x < y : (incorrect operator)

line:27:error: z = x > y : (incorrect operator)

line:34:error:  x&&y : (incorrect operator)

