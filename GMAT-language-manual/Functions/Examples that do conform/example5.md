## ***Example 5***

* Recursion and static variables

```js
add_library :+ io.LIB

fib:_num argument:_num 
    static _num var = 0 ;
    var+=1
    write(var,"(",x,") ")
    if(argument == 1 || argument ==2)
        return 1
    return fib(n-1)+fib(n-2)


main::_num
    write("Enter the number:")
    _num x
    read(x)

    _num a
    a = fib(x)
    write("/n")
    write("fibonocci number = ",a,"\n")
```

INPUT:
6

OUTPUT:
1(6) 2(5) 3(4) 4(3) 5(2) 6(1) 7(2) 8(3) 9(2) 10(1) 11(4) 12(3) 13(2) 14(1) 15(2) 
fibonocci number = 8

~~Function syntax ==> function:arg1,arg2...:ret_type1,ret_type2....
~~static varaibles preserve their values in their scope, and are not initialised again in their new scope

