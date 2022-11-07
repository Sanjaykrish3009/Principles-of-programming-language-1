## ***Example 3***

* Header Files ,Libraries
io.LIB, geo.LIB, plotG.LIB are some examples of header files in gmat

```js
add_library <io.LIB>
main::_num
    _num x1,y1,x2,y2,x3,y3
    write("give the co-ordinates of triangle:")
    read(x1,y1,x2,y2,x3,y3)

    _polygon triangle = [x1,y1;x2,y2;x3,y3]
    _num a,b
    (a,b) = circumcenter(triangle) 
```

~~ add_library must strictly be followed by a :+ and the library name,
   add_library :+ io.LIB   is correct implementation
~~ for the working of above written code you must also include geo.LIB library
~~ the datatype _polygon and its corresponding functions are present in  
   geo.LIB , so you must add_library :+ geo.LIB for suucessful compilation.   





