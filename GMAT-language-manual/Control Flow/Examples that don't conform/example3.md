##  ***Example 3***

* while loop

```js
add_library :+ io.LIB  
add_library :+ plotG.LIB

main::_num
    
    _polygon T
    _num x1,x2,x3,y1,y2,y3
    
    write("Enter the coordinates of the triangle:")
    read(x1,y1,x2,y2,x3,y3)
    T=[x1,y1;x2,y2;x3,y3]

    while: Area(T) > 10  
        ~Arguments for the function Plotgraph should always be parsed using square brackets~
        Plotgraph(T) 
        write(Area(T))
        T=Medialtriangle(T)
        ~Medial triangle id triangle formed with mid points. ~

    return 0
```

* OUTPUT:

line:18:error: while: Area(T) > 10 : (function not defined or librabry was not added)

line:20:Plotgraph(T) : (Plotgraph(T), expecting different bracket)

line:22:error: while: T=Medialtriangle(T) : (function not defined or librabry was not added)






