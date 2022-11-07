## ***Example 3***

```js
add_library :+ io.LIB
add_library :+ geo.LIB

~~formatted input/output

main::_num

    _num x,r,c
    write("enter the number x: ")
  ~the number of digits after the decimal to be scanned should always be enclosed in brackets~
    read(0.3x)
    write("number entered is: ",x,"\n")

    write("enter the radius r: ")
  ~~reads the value of r
    read(r)
  ~~prints the formatted value of r
  ~~decimal part of r value is rounded off to 3 digits
    write("radius entered: ",(0.3)r,"\n")
  ~~getcircumference calculates the circumference of the circle with radius r
  ~arguments for all other functions except plotting should be parsed using circular brackets~
    c = getcircumference[r]
  ~~decimal part of circumference value is rounded to 5 digits
    write("circumference of the formed circle: ",(0.5)c,"\n")

    _str s
    write("enter the string:")
    read(s)

  ~(a.b.c) prints a formatted string- (a) spaces at the beggining, (c) spaces at the end and (b) is the max no.of characters it can print~
  ~For a string, if there is no need of printing the space at the start or end also, you shpould
    write("the entered string is: ",(6.7)s,":")
    return 0
```


OUTPUT :

line:14:error:read(0.3x) :(error expected in "0.3x")

line:25:error:c = getcircumference[r] : (getcircumference[r], expecteing different bracket)

line:35:error: write("the entered string is: ",(6.7)s,":") : ((6.7) should be in the format (a.b.c))
