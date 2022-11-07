## ***Example 2***

```js
add_library :+ io.LIB
add_library :+ geo.LIB 

main :: _num

    _polygon T
    _num x1 = 0,x2 = 8,x3 = 0,y1 = 0,y2 = 0,y3 = 8

    T=[x1,y1;x2,y2;x3,y3]
  ~~prints the properties of the polygon T
    write(getproperties(T))

    return 0
```


output:

This is a right angled isosceles triangle

sides are 8,8,11.3137

centroid:{2.666,2.666}

orthocentre:{0,0}

circumradius:5.65685

circumcentre:{4,4}

incentre:{2.34315,2.34315}

inradius:2.34315

altitude(from hypotenuse):5.65685

perimeter:27.3137

area:32 sq.units

