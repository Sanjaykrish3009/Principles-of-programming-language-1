### Example 4

* This example shows some conic data-types

```js
add_library :+ io.LIB
add_library :+ geo.LIB
~geo.LIB consists the class functions related to conics ~

main::_num
  _str expression

  read(expression)
~input expression is compared with
    ax^2 + 2hxy + by^2 + 2gx + 2fy + c
    NOTE: x,y are considered as co-ordinates, so use other names for variables~

~conic datatype takes the expression as input and returns its properties as output ~
  _conic variable

~expression is processed by the compiler after injection
       it returns basic properties of the conic to the variables
       they can be accessed by simple inbuilt functions as shown~
  variable.inject(expression)

~returns a string; describing the shape of expression~
  write(variable.shape)   

~it returns a _num type ; giving the eccentricity of conic~
  write(variable.eccentricity)


~Prints out information about all properties~
  write(variable)
  return 0

```
