## ***Example 4***

```js
~~file access

add_library :+ io.LIB

 main::_num
    _num a,b,c,d,distance
    ~~ datatype point
    _point p1,p2

    ~declaration of a file pointer~
    FILE *fp, *fpr

    ~while opening a file it should be mentioned in which mode should we open it i.e either read or write~
    fp = fopen(input.txt)
    fpr = fopen(output.txt, "w")

    ~while reading from a file or writing in a file, file pointer should be mentioned in fread and fwrite~
    fread(a,b,c,d)
    p1 = [a,b], p2 = [c,d]
    distance = getdistance(p1,p2)
    fwrite(fpr,"The distance between the given points is ", distance)
    fclose(fpr)
    return 0;
```




OUTPUT   

line:17:error: fp = fopen(input.txt) : (did not mention the mode of the file)

line:21:error: fread(a,b,c,d) : (file pointer is missing)

line:23:error: distance = getdistance(p1,p2) : (function not defined or library was not added)

line:warning : file(fp) was not closed
