## ***Example 3***

* pointers in function arguements

```js
add_library:+io.LIB

main::_num
    _num n
    write("enter degree of the equation :")
    read(n)
    _num Arr[n]
    write("\nenter the roots of the equation ")
    for:i = 0,i<n:i++
      read(Arr[i])
    ~~In the function the argument is a pointer (*Arr)
    write("\ncoefficients of the equation are: ",) 
    getequation(Arr)
    
    return 0
```
    




OUTPUT :

line:14:error:for:i = 0,i<n:i++ : (variable i was not declared)

line:15:error:read(Arr[i]) : (variable i was not declared)

line:18:error: getequation(Arr) : (incorrect arguement)

