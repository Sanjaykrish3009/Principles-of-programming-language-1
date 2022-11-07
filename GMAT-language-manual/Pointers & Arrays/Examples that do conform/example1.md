## ***Example 1***

* pointers and addresses

```js
add_library:+ io.LIB

main::num
  _num a,b, *ip, A[10]
  write("Enter the value of a: ")
  read(a)
  ~~ ip stores the address of a
  ip = &a
  ~ b gets the value stored in the address that ip is pointing to ~
  b = *ip
  (*ip)++3
  ~~ *ip is a
  ~~ (*ip)++3 is in the format x++y => x=x+y, which means a=a+3
  write("\naddress of a is :",ip)
  write("\nnew value of a is",a)
  write("\nb value is",b)
  ~~ now ip stores the address of the array
  ip = &A[0]
  ~~ Now with ip, whole array can be accessed 
  ~~ *(ip+1), *(ip+2) => A[1],A[2]
  write("\naddress of A[5]: ",ip+5)
  return 0
  ```


  OUTPUT :
  
  a value: 3
  
  address of a is : 217564
  
  new value of a is 6
  
  b value is 3
  
  address of A[5]: 265389


