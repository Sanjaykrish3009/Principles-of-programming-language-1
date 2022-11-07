##  ***Example 2***

* for loop

```js
add_library :+ io.LIB 

main::_num
    _num n
     write("Enter the number of elements of array:")
     
    _num Array[n]
    write("Enter the elements of array:")

    for:_num(i=0),i++:i<n:
        read(Array[i])

    for:_num(i=0), i++:i<n:
        for:_num(j=i+1), j++: j<n:
            if:Array[i] > Array[j]
            _num temp = Array[i]
            Array[i] = Array[j]
            Array[j] = temp
    
    write(Sorted array:)

    for:_num(i=0),i++:i<n:
        write(Array[i]," ")            

    return 0
```

* OUTPUT:

line:21:error: _num temp = Array[i]

line:22:error: Array[i] = Array[j] (indentation error,expected an indented block)

line:23:error: Array[j] = temp (indentation error,expected an indented block)

line:25:error: write(Sorted array:) (variable not found, error in "Sorted array:")






