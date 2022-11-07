##  ***Example 1***

* Using string data-type

```js
~~single line comment
~multi line comment~

~syntax to add libraries ==> add_library :+ 'library name'~
add_library :+ io.LIB
~NOTE: there should be no space between : and + ~

~function format ==> function:arg1,arg2:ret_type1,ret_type2 ~
~if more than one argument or return type, you need to place a "," in between~
main::_num
  _str x    
  x = "hello world 2.0"  
~string data type is used to store a sequence of characters ~
  write(x)
~write function prints everything stored in the variable ~
  return 0
```
