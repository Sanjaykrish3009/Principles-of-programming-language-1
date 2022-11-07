##  ***Example 5***

* Bitwise operators

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

  z = x << y                    ~~leftshift
  write(z,"\n")

  z = x >> y                    ~~rightshift
  write(z,"\n")

  z = $x                            ~~negation
  write(z,"\n")

  return 0
```

* OUTPUT:
14
1
15
3584
0
-8
