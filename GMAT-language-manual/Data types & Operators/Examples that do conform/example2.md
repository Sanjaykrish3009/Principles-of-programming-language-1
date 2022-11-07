##  ***Example 2***

* Datatypes

```js
~Datatypes~

add_library :+ io.LIB 

main::_num

    _num x1 = 5 ,y1 = 5.5
    _num x2 = 10.5, y2 = 10.5
    _num x3 = -12.25, y3 = -6

    _str y = {'a','e','3'}  

    _point p1,p2

    p1 = [x1,y1]
    p2 = [x2,y2]
    p3 = [x3,y3]

    _polygon A = [p1;p2;p3] 
    ~A is a triangle ~
    ~A can be also defined in this way "A = [x1,y1;x2,y2;x3,y3]"  ~
    

    _conic var 
    
    var.inject(1,0,1,0,0,-9)

    ~conics general equation ax^2+2hxy+by^2+2gx+2fy+c~
    ~Here var is a circle with centre origin and radius 3 ~

    _poly Eq:3
    ~This implies Eq is a polynomial with degree 3~
    Eq = [1,-3,3,-1]
    ~~ 1,-3,3,-1 are coefficients of polynomial 

    return 0

~~ _num allocates memory according to the value assigned to the variable
~~ _str datatype is used to store charaters and strings
~~ _point datatype is used to store coordinates
~~ _polygon takes co-ordinates as input 
~~ _conic datatype takes the coefficients of the equation defining conic as input.Coefficients must be given in the order [a,h,b,g,f,c] where 
ax^2+2hxy+by^2+2gx+2fy+c is the general equation of conics.
~~_poly datatype takes the coefficients of polynomials as inputs and return the roots of the polynomial equation(if roots are imaginary it returns "und")    
~~_polygon , _conic, _poly datatypes input is given inside "[]" these brackets only.
```
