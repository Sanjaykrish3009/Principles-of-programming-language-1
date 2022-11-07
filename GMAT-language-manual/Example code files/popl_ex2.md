## ***Example 2***

* This example focuses on Syntax of loops

```js
add_library :+ io.LIB

main:: _num
~variables can be declared and initialised at same time~
~Gmat usesindentation;extra tab space is to be added at beggining of function/loops~
  _num a=0,r=0,n=0
~by default variables are initialised to 0 and pointers are initialised to NULL~
  read(a,r,n)
  _num A[n]

~for loop syntax ==> for:initialize,termination:increment/decrement~  
  for:_num(i=0),i<n:i++
     A[i] = a*pow(r,i)

~while loop syntax ==> while:condition~
  _num j=0
  while:j<n
    _num temp = A[j+1]
    A[j+1] = A[j]
    A[j] = temp
    j++

  write(A)
  return 0
```
