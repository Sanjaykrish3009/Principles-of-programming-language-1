## ***Example 2***

* pointers in function arguements

```js
add_library:+io.LIB

main::_num
  _num n
  write("enter degree of the equation :")
  read(n)
  _num Arr[n]
  write("\nenter the roots of the equation ")
  for:_num (i = 0),i<n:i++
    read(Arr[i])
  ~~In the function the argument is a pointer (*Arr)
  write("\ncoefficients of the equation are: ",) 
  getequation(*Arr)
  return 0
```



  OUTPUT 1:
  enter degree of the equation : 3
  enter the roots of the equation 1 2 3
  coefficients of the equation are: 1 -6 11 -6

  OUTPUT 2:
  enter degree of the equation : 2
  enter the roots of the equation 21 -5 
  coefficients of the equation are: 1 -16 -105
