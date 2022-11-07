## ***Example 3***

* Header Files ,Libraries
io.LIB, geo.LIB, plotG.LIB are some examples of header files in gmat

```js
add_library :+ io.LIB 
main::_num
    _str name[20]
    write("Enter your name:")
    read(name)

    write("hello",name," welcome to gmat programming!!")
```

INPUT:
xlr8

OUTPUT:
hello xlr8 welcome to gmat programming!! 

~~ io.LIB library contains the standard input output functions like write(),      read()...etc
~~ geo.LIB contains the geometric functions
~~ plotG.LIB helps you to plot the geometric data 
~~ without the libraries, for the code to run you need to write the functions     yourself!!

