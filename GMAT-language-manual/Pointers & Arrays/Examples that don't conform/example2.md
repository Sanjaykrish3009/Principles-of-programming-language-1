## ***Example 2***

* pointers and arrays

```js
add_librabry:+io.LIB 
~~ function:function arguments:return type
~~ function arguments are pointers
~~ arguemnt given in this function is a pointer

search: void array, _num arr_size, _num element:_num
  for:_num(i=0),i++:i<arr_size:
    if : array[i] == element
      return 1
  return 0  


main::_num
    _num n,element
    write("size of the array:")
    read(n)
    _num Array[n]

    for:_num(i=0), i++:i<n
      read(A[i])
    write("enter the value to be searched: ")
    read(element)
    
    ~~ function(function arguments)
    _num value = search(*Array,n,element)
    if : value = 1
      write("given",element,"is in the array")
    else
      write("given",element,"is not in the array")
    return 0
```

OUTPUT :

line:11:error:search: void array, _num arr_size, _num element:_num: (incorrect arguement-void array)

line:31:error:if : value = 1 : (use '==' to turn this assignment into an equality comparison)


