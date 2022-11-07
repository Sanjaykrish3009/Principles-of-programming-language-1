##  ***Example 4***

* while loop

```js
add_library :+ io.LIB 
add_library :+ geo.LIB 
add_library :+ plotG.LIB

main::_num
    
    _polygon T
    _num x1,x2,x3,y1,y2,y3
    
    write("Enter the coordinates of the triangle:")
    read(x1,y1,x2,y2,x3,y3)
    T=[x1,y1;x2,y2;x3,y3]

    while: Area(T) > 10  
        Plotgraph [T] 
        write(Area(T))
        T=Medialtriangle(T)
        ~Medial triangle is triangle formed with mid points of the sides as new vertices ~

    return 0
```

* EXAMPLES:

INPUT1:
-3 10 -3 -8 9 -8

OUTPUT1:
(Figure will be plotted)
108
27




