## ***Example 5***

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
            read(Mat1[i]j])
   
    
    write("Enter the elements of 2nd matrix:\n")
   
    ~~Taking input of 2nd mtrix from user
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
        write("Enter Mat2[",i,"]","[" j,"] value:")
        read(Mat2[i][j])

    ~~adding both matrices
    for:_num(i=0),i++:i<m
        for:_num(j=0),j++:j<n
            Sum[i][j]=Mat1[i][j]+Mat2[i][j]
    
    write("Resultant Matrix:")
    
    ~~printing Resultant matrix
    for:_num(i=0),i++:i<m
        write("\n")
        for:j=0,j++:j<n           
            write("Sum[i][j] ")
    
    return 0
```


OUTPUT :

line :26:error: read(Mat1[i]j]) : (expecting a bracket)

line :34:error: write("Enter Mat2[",i,"]","[" j,"] value:") : (indentation error,expected an indented block)

line :34:error: write("Enter Mat2[",i,"]","[" j,"] value:") : (expecting a ',')

line :35:error: read(Mat2[i][j]): (indentation error,expected an indented block)

line :47:error: for:j=0,j++:j<n : (variable j was not declared)

line :48:error: write("Sum[i][j] ") :  (variable j was not declared)


