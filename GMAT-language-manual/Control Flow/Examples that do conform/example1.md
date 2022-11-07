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
    else if : BMI@[18.5,25)  ~BMI lies between [18.5,25)~
        write("Normal\n")
    else if : BMI@[25,30)   
        write("Overweight\n")
    else : 
        write("Obesity\n")
       
    return 0
```

* EXAMPLES:

INPUT1:
1.64 50

OUTPUT1:
18.59
Normal

INPUT2:
1.67 74

OUTPUT2:
26.53
Overweight




