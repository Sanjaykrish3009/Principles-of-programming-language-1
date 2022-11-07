##  ***Example 2***

* Datatypes

```js
add_library :+ io.LIB 

main::_num

    ~variable of datatype _num can not take characters~
    _num x1 = h ,y1 = l                                 
    _num x2 = 10.5, y2 = 10.5
    _num x3 = -12.25, y3 = -6

    ~characters should always be mentioned in single quotes~
    _str y = {'a','e',"3"}  

    ~coordinates of one point should always be differentiated with a semi-colon(;)~
    _polygon A = [x1,y1,x2,y2,x3,y3] 

    ~A is a triangle ~

    _conic var 
    
    ~coefficients of a conic should always be given in the order of a,h,b,g,f,c even if they are equal to 0~
    var.inject(1,1,-9)

    ~conics general equation ax^2+2hxy+by^2+2gx+2fy+c~
    ~Here var is a circle with centre origin and radius 3 ~

    ~degree of a equation should always be mentioned~
    _polynomial Eq : 2
    ~This implies Eq is a polynomial with degree 3~
    Eq = [1,-3,3,-1]
    ~~ 1,-3,3,-1 are coefficients of polynomial 
```

* OUTPUT

line:11:error: _num x1 = h : (invalid datatype)

line:11::error: _num y1 = l : (invalid datatype)

line:16::error: _str y = {'a','e',"3"} : (characters should be in single quotes)

line:26::error: var.inject(1,1,-9) : (expected more number of arruguments)

line:32::error: _polynomial Eq:2 : (datatype polymonial not found)

warning: (main function did not return) 
