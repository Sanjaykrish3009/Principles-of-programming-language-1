## ***Example 5***

* pointer arrays

```js
add_library :+ io.LIB 
add_library :+ geo.LIB

main::_num 
    
    _num n
    write("Enter the number of coordinates:")
    read(n)

    _polygon *Tri[3]
    ~~array of pointers that points to triangles
  
    _point pt[6]
    ~~ pt is an array of coordinates

    for : _num(i=0),i++:i<n
        _num x,y
        read(x,y)  ~~taking input from user
        ~incorrect format for taking point as input~
        pt[i] = (x,y)
    

    for : _num(i=0),i++:i<3
        ~incorrect format for rand~
        _num j = rand % n  
        if: j+2 < n    
            *Tri[i] = [pt[j];pt[j+1];pt[j+2]]
      ~Tri[i] stores the address of a triangle formed by 3 consecutives coordinates in the array~
        else:
            i--
 
    Check_Congruence(Tri[0],Tri[1])
    Check_Congruence(Tri[1],Tri[2])
    Check_Congruence(Tri[2],Tri[0])
    ~~Check_Congruence is a function with 'polygon' as arguements
    
    return 0
```

   
OUTPUT :

line:22:error : pt[i] = (x,y) : (incorrect brackets) 

line:27:error:_num j = rand % n  :(incorrect format, expecting a bracket)

line:34:error:Check_Congruence(Tri[0],Tri[1]) : (wrong arguement was entered)

line:35:error:Check_Congruence(Tri[1],Tri[2]) : (wrong arguement was entered)

line:36:error:Check_Congruence(Tri[2],Tri[0]) : (wrong arguement was entered)



