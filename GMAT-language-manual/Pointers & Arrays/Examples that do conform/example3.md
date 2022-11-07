## ***Example 3***

* pointers and arrays

```js
add_librabry:+io.LIB 
~~ function:function arguments:return type
~~ function arguments are pointers
search: void *array, _num arr_size, _num element:_num
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
  if : value == 1
    write("given",element,"is in the array")
  else
    write("given",element,"is not in the array")
return 0
```


OUTPUT 1:

size of the array: 5

3 4 1 6 0

enter the value to be searched: 4

4 is in the array


OUTPUT 2:

size of the array: 10

34 21 7 4 53 0 27 18 2 76

enter the value to be searched: 100

100 is not in the array

