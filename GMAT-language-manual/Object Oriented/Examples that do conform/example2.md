###    ***EXAMPLE 2***

* explaining multiple Inheritance: A class being derived from more than one base class.

```js

add_library :+ io.LIB
add_library :+ geo.LIB

class parentA
    public:
        parentA::
            write("constructer of A is called.\n")
        getperimeter:_polygon x:
            write(perimeter(x),"\n")
class parentB
    public:
        parentB::
            write("constructer of B is called.\n")
        getarea:_polygon x:
            write(area(x),"\n")

class childC: import public parentA, import public parentB
    public:
        childC::
            write("constructer of C is called.\n")
        getcentriod:_polygon x:
            write((0.3)centriod(x))

main::_num
    childC variable
    _polygon triangle = [0,0,6,0,0,8]

    variable.getcentriod(triangle)
    varaible.getarea(triangle)
    varaible.getperimeter(triangle)

```
OUTPUT:

constructer of A is called

constructer of B is called

constructer of C is called

2 2.67

24

24

* class childC: import public parentB, import public parentA
* if this was the order, constructer of B would be called first and then of A
