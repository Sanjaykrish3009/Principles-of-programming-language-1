## ***Example 6***

* gmat preprocessors

~~ add_library , define are two preprocessors of gmat

~~ instead of standard libraries like io.LIB, geo.LIB gmat allows you to write create your own libraries. you can add them either statically or dynamically.

new.LIB 

#ifndef LIB_FILE

#define LIB_FILE 

comparision:arguments:_num 

#endif

new.gm

~~ contains the required type of comparision function
```js
comparision:_str x[],_str y[]:_num
    _num i = 0
    while:x[i]!='\0' && y[i]!='\0'
        if:x[i]<y[i]
            return 1
        else if:x[i]>y[i]
            return -1
    if:x[i]=='/0' && y[i]=='/0
      return 0
    else if: x[i]=='/0'
      return 1
    else 
      return -1          
return 0
```

```js
add_library :+ io.LIB 
add_library :+ new.LIB 
main::_num 
    ~~ here you can now directly call the comparision function
    _str array1[], array2[]
    write("Enter the two strings:")
    read(array1,array2)
    write(comparision(array1,array2))
return 0
```

INPUT:
abcdef abcder

OUTPUT:
1

INPUT:
qwerty qwe 

OUTPUT:
-1

~~ #ifndef -makes sure that LIB_FILE is defined only once




