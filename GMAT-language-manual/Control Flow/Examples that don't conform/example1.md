##  ***Example 1***

* If - Else if

```js
add_library :+ io.LIB

main::_num
    
    _num BMI,ht,wt
    write("Enter your height(in m) and weight(in kg) respectively:")
    read(ht,wt)

    BMI= wt/(ht*ht)
    write((0.2)BMI)

    if: BMI < 18.5
        write("Underweight\n") 
    ~range of a variable should always be mentioned in "VARIABLE@(range of the variable)" format~
    else if : 18.5 <= BMI < 25  
        write("Normal\n")
    ~range of a variable should always be mentioned in "VARIABLE@(range of the variable)" format~
    else : 25 <= BMI < 30    
        write("Overweight\n")
    else : 
        write("Obesity\n")
       
    return 0
```

* OUTPUT:

line:20:error:else if : 18.5 <= BMI < 25 : (incorrect format)

line:23:error:else if : 25 <= BMI < 30 : (incorrect format)

line:23:error:else : 25 <= BMI < 30 : (unnecessary condition for else)

line:25:error:else : else :  : (corresponding if statement is not found)






