## ***Example 4***


```js
add_library :+ io.LIB 
add_library :+ geo.LIB

catch:_str x:
    if:x
    write("invalid exception caught! at level ",level(throw),"\n")

class mainclass
        private:
            _num numerator,denominator

        public:
                mainclass::
                mainclass:num,denom:
                    numerator = num
                    denominator = denom

                _num divide::
                        if:denominator = 0 throwexpt:invalid
                        return numerator/denominator


main :: _num 

    mainclass divisionclass
    _num x,y,result
    write("enter numerator: ")
    write("enter denominator: ")
    divisionclass:x,y:
    result = divisionclass.divide:
    write("result is :",result,"\n")

    mainclass divisionclassprime(17,0)
    result = divisionclassprime.divide:
    write("result is :",result,"\n")
```


OUTPUT:
enter numerator: 5
enter denominator: 12
result is : 0.4166667

invalid exception caught at level divide in mainclass type





