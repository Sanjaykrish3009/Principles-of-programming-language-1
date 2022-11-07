##  ***Example 7***

* Precedence of operators

Operators and their Associativity

@, from left to right

() [] -> ., from left to right

! ~ ++ -- + - * (type), from right to left

sizeof

* / %, from left to right

+ -, from left to right

<< >>, from left to right

< <= > >=, from left to right

== !=, from left to right

&, from left to right

^, from left to right

|, from left to right

&&, from left to right

||, from left to right

= += -= *= /= %= &= ^=, from right to left

|= <<= >>= 

,, from left to right


```js
add_library :+ io.LIB


main::_num

_num p=2,n=1
_num x=7
_num y= (x >> (p+1-n)) & $(2 << n);

if:y
    write("condition1 is satisfied!!")
if:5^3+4/2*3%2&6@[6,10)
    write("condition2 is satisfied.")    

return 0
```



OUTPUT:
condition1 is satisfied!!

condition2 is satisfied.







