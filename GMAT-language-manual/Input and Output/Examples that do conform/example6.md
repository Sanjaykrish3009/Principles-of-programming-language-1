## ***Example 6***

* Miscellaneous functions

Mathematical functions (sinx,cosx,tanx...etc)

String functions(strcpy,strcmp,strcat..etc)

Geometric functions:

In the following, A,B are defined with _polygon datatype

Following functions take _polygon as arguments

area(A)             -returns area of A

perimeter(A)        -returns perimeter of A

numberofDiagonals(A)-returns number of diagonals in A

numberofSides(A)    -returns number of sides in A

typeofTriangle(A)   -prints the type of triangle if A is
                     a traingle, else return
                     
center(A)           -returns coordinates of center of A

orthocenter(A)      -returns coordinates of Orthocenter 
                     of A if A is triangle, else return
                     
circumradius(A)     -returns the Circumradius of A if A 
                     is triangle, else return
                     
circumcenter(A)     -returns coordinates Circumcenter 
                     of A if A is triangle, else return
                     
getPropeties(A)     -prints all the above properties 
                     basing on polygon type of 'A'
                     
check_Congruence(A,B)-prints "TRUE" if congruent,else   
                     "FALSE"

Conic functions:

In the following A,B are defined with _conic datatype

Following functions take _conic as arguments

focii(A)             -returns coordinates of focii of A 

eccentricity(A)      -returns eccentricity of A 

focalLengh(A)        -returns focal length of A

lenghofmajoraxis(A)  -returns length of majoraxis of A

latusrectum(A)       -returns length of latusrectum of A

conicProperties(A)   -prints all  above properties of A

typeofconic(A)       -prints type of conic A is

Polynomial functions:

In the following A is defined with _poly, 
B is an array  of roots of a polynomial

solve(A)             -returns the roots of A

getequation(B)       -prints the coeffients of 
                      polynomial whose roots are in array B

```js
add_library :+ io.LIB

main::_num

    _point pt1, pt2, pt3
    _polygon T
    write("Enter the coordinates of the triangle in the order (x1,y1), (x2,y2), (x3,y3) : ")
    read(pt1,pt2,pt3)
    T = [pt1, pt2, pt3]

    typeofTriangle(T)
    write("\nPerimeter of the triangle is ",(0.2)Perimeter(T))
    write("\nArea of the triangle is ",Area(T))
    _num x,y = Center(T)
    write("The centrid of the triangle ",(0.2)x," ",(0.2)y)
    x,y = Circumcenter(T)
    write("The Circumcenter of the triangle ",x," ",y)
    return 0
```


OUTPUT :

Enter the coordinates of the triangle in the order (x1,y1), (x2,y2), (x3,y3) : 0 0 8 0 0 8 

Triangle is a right angled triangle

Perimeter of the triangle is 27.31

Area of the triangle is 32

The centrid of the triangle 2.67 2.67

The Circumcenter of the triangle 4 4


