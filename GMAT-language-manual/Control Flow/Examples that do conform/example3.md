##  ***Example 3***

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
    
    write("Sorted array:")

    for:_num(i=0),i++:i<n:
        write(Array[i]," ")            

    return 0
```

* EXAMPLES:

INPUT1:
10
3 7 9 5 10 6 1 4 2 8

OUTPUT1:
1 2 3 4 5 6 7 8 9  10 
 
INPUT2:
5
-2 0.05 1.4 2.6 -3.2

OUTPUT2:
-3.2 -2 0.05 1.4 2.6



