## ***Example 6***

* multidimensional array
  addition of two matrices

```js
add_library :+ io.LIB 

main::_num
    
    _num m,n
    write("Enter the order of matrices to be added:")
    read(m,n)

    _num Mat1[m][n],Mat2[m][n], Sum[m][n]
    ~Mat1,Mat2,Sum are 2 dimensional arrays initialised with '_num' datatype~
    ~Similarly, Mat1[i][j][k] is a 3d array


    write("Enter the elements of 1st matrix:\n")

    ~~Taking input of 1st mtrix from user
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            write("Enter Mat1[",i,"]","[",j,"] value:")
            read(Mat1[i][j])
   
    
    write("Enter the elements of 2nd matrix:\n")
   
    ~~Taking input of 2nd mtrix from user
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            write("Enter Mat2[",i,"]","[",j,"] value:")
            read(Mat2[i][j])

    ~~adding both matrices
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            Sum[i][j]=Mat1[i][j]+Mat2[i][j]
    
    write("Resultant Matrix:")
    
    ~~printing Resultant matrix
    for:_num(i=0),i++:i<m
        write("\n")
        for:_num(j=0),j++:j<n           
            write("Sum[i][j] ")
    
    return 0
```



    OUTPUT:
    Enter the order of matrices to be added:2 3
    Enter the elements of 1st matrix:
    Enter Mat1[0][0] value: 10 
    Enter Mat1[0][1] value: -2.3
    Enter Mat1[0][2] value: 5
    Enter Mat1[1][0] value: 6.67
    Enter Mat1[1][1] value: 9
    Enter Mat1[1][2] value: -7
    Enter the elements of 2nd matrix:
    Enter Mat2[0][0] value: -3
    Enter Mat2[0][1] value: -3.4
    Enter Mat2[0][2] value: 8
    Enter Mat2[1][0] value: -1.3
    Enter Mat2[1][1] value: 4
    Enter Mat2[1][2] value: -2
    Resultant Matrix:
    7 -5.7 13
    5.37 13 -9





