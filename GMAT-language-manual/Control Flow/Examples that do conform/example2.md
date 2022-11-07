##  ***Example 2***

* switch case

```js
add_library :+ io.LIB 

main::_num
    
    _num N 
    write("Enter the number of verices of a polygon:")
    ~N should be postive~
    read(N>0) 
    ~~read function prompts the user till user enters valid input(special feature) 
    ~~write function also follows the same
    
    switch : N
        case : 1 : write("point\n")
                   break
        case : 2 : write("line\n") 
                   break
        case : 3 : write("triangle\n")
                   break 
        case : 4 : write("quadrilateral\n")
                   break
        case : 5 : write("pentagon\n") 
                   break
        case : 6 : write("hexagon\n")
                   break
        case : 7 : write("heptagon\n") 
                   break
        case : 8 : write("octagon\n")
                   break 
        case : 9 : write("nonagon\n")
                   break
        case : 10 : write("decagon\n") 
                   break           
        default : write(N,"-sided polygon")           
    ~Implement range in switch case~

    ~Can be implemented for strings as well~
    return 0
```

* EXAMPLES:

Input1:
4

Output1:
quadrilateral

Input2:
-3 (Since, the given input is invalid, it won't be considered, so user should enter - speciality of read function)
7 (It will be considered, since it is valid input)

output2:
heptagon


