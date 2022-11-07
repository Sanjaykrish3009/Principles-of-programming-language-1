
## ***Example 3***

* Finding roots of a quadratic equations

```js
~ finding roots for a quadratic equation ~
add_library :+ io.LIB
add_library :+ geo.LIB

main::_num

~_poly is the data type to define the polynomial equations with degree~
~_num is a type specifier
  it includes all four basic arthematic type specifiers in C
  It uses dynamic binding to allocate space to the declared variable~
  _poly Eq:2
  _num a, b, c  
~if not initialised all variables are set to Zero~  
~write(a,b,c)  --> at this point would give out 000 as output~

  write("input co-eff of quad")
  read(a,b,c)
~inserting the coefficients to the equation~
  Eq = [a,b,c]
  _num x,y

~solve(polynomial equation | variable) gives the roots of the equation written
    note that if b^2-4a*c<0 ; 'und - undefined' will return into x,y ~


  (x,y) = solve(Eq)
  write("roots are:",x,"and",y)
  return 0
