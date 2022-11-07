## ***Example 5***

* Intro to polygon datatype and plotting

```js
~Finding centroid of the polygon~
add_library :+ io.LIB
add_library :+ plotG.LIB
~plotG.LIB library allows you to open plot windows/tabs~

main :: _num
  write ("Enter the coordinates of the triangle:")
  _num x1, y1, x2, y2, x3, y3
  read(x1,y1,x2,y2,x3,y3)

~input to polygon, given in the form of points~
~polygon is a datatype, used to store end point co-ordinates of polygon~
  _polygon A = [x1,y1;x2,y2;x3,y3]

~three points that is triangle is given as input~
~side_len() returns the sidelengths of the polygon~
  _num a,b,c
  (a,b,c) = side_len(A)
~(...arg) = side_len(A) number of arguments should not be less~
  write(a,b,c)
~prints all sides of polygon A ~

~ finding the type of the triangle(acute/right/obtuse) ~
  _str B = type[triangle(A)]
~type[] returns a string, donot store the value in _num type variables~

  _num x4,y4
  (x4,y4) = centroid(A)
~() = centriod(A) ; make sure correct number of arguments are provided and they are enclosed by brackets~

  write("A is ")
  write(B,"\n")     ~ \n for new line
  write("Centroid of the triangle : ")
  write("(",x4,",",y4,")")
~plotting the polygon on a 2D plane~
  Plotgraph[polygon(A),centroid(A)]
  return 0

```
