## ***Example 5***

```js
~~file access

add_library :+ io.LIB 
add_library :+ geo.LIB

 main::_num
    _num a,b,c,d,distance
    ~~ datatype _point, which is the cordinate of point(x,y)
    _point p1,p2
    ~~Declaration of file pointer
    FILE *fp, *fpr
    ~~ Opening the files
    fp = fopen(input.txt, "r")
    fpr = fopen(output.txt, "w")
    ~~ reads the input fro input.txt file
    fread(fp,a,b,c,d)
    ~~ assining the points and calculating the distance between them
    p1 = [a,b], p2 = [c,d]
    distance = getdistance(p1,p2)
    
    ~~ prints the distance between points in the output.txt file
    fwrite(fpr,"The distance between the given points is ", distance)

    ~~close the files
    fclose(fp)
    fclose(fpr)
    return 0;
```








INPUT FILE

input.txt
1 2
3 4


OUTPUT FILE

output.txt
The distance between the given points is 1.414


 



