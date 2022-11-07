## ***Example 1***

* ~~ pointers and addresses

```js
add_library:+ io.LIB

main::num
  _num a,b,A[10]

  _num* ip1,ip2
  ~Here ip2 is not a pointer.'_num*' doesnt apply to all variables(only for first variable)~
  ~pointers should not be initialised in this way.It should be "_num *ip1, *ip2"~

  write("Enter the value of a: ")
  read(a)
  ~~ ip1 
  stores the address of a
  ip1 = &a

  ~ b gets the value stored in the address that ip2 is pointing to ~
  b = *ip2 ~(ERROR) ip2 is initialised with _num but not as a pointer type~
  
  (ip1*)++3  ~~(ERROR) it should be (*ip1)++3
  
  write("\naddress of a is :",ip)
  write("\nnew value of a is",a)
  write("\nb value is",b)

  ip = A[0]
  ~ Here ip is storing the value of A[0],it cant access array 'A'~
  ~Inorder to access array 'A', it should be returned with address of array.That is, "ip=&A[0]"~

  
  write("\naddress of A[5]: ",ip+5)
  ~Technically Incorrect output~

  return 0
```


OUTPUT :

line:22:error:b=*ip2 : (ip2 is not a pointer type )

line:24:error:(ip1*)++3 : (ip1* is invalid use of pointer type )


