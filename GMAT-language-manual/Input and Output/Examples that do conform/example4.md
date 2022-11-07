## ***Example 4***

```js
add_library :+ io.LIB
add_library :+ geo.LIB

~~formatted input/output

main::_num

    _num x,r,c
    write("enter the number x: ")
    read((0.3)x)
    write("number entered is: ",x,"\n")

    write("enter the radius r: ")
  ~~reads the value of r
    read(r)
  ~~prints the formatted value of r
  ~~decimal part of r value is rounded off to 3 digits
    write("radius entered: ",(0.3)r,"\n")
  ~~getcircumference calculates the circumference of the circle with radius r
    c = getcircumference(r)
  ~~decimal part of circumference value is rounded to 5 digits
    write("circumference of the formed circle: ",(0.5)c,"\n")

    _str s 
    write("enter the string:")
    read(s)

  ~(a.b.c) prints a formatted string- (a) spaces at the beggining, (c) spaces at the end and (b) is the max no.of characters it can print~
  
    write("the entered string is: ",(6.7.10)s,":")


  return 0
```

OUTPUT:

enter the number x: 8.3975345

number entered is: 8.398

enter the radius r: 5.674599

radius entered: 5.674

circumference of the formed circle: 35.65456

enter the string:Hello,world

the entered string is: (6_spaces)hello,w(10_spaces):


