## ***Example 3***  


```js
~~polymorphism

~~function overloading in GMAT


add_library :+ io.LIB 


printpretty:_num number:_num
    write(number,"is of type ",typeof(number),"\n")

printpretty:_str somestring:_str
    write("\"",somestring,"\"is of type ",typeof(somestring),"\n")


main::_num

    _num number
    write("enter some number: ")
    read(number)
    printpretty:number:


    _str s 
    printpretty(number)
    write("enter some string: ")
    read(s)
    printpretty:s:

    return 0
```


OUTPUT:
enter some number: 10.445
10.445 is of type number

enter some string: This is gmat language
"This is gmat language" is of type string_literal




