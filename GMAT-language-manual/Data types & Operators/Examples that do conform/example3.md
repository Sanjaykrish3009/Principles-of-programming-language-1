##  ***Example 3***

* Arthimetics operators:  +,-,*,/,%  

```js
add_library :+ io.LIB 

main::


    ~~precedence order is same as in all languages
    ~~ parsing is done from left to right 

    _num x=0,y=0

    x = 3+4*5/2*8%2
    y = 3+4/2*5+8%3

    write(x," ",y)

    return 0
```

* OUTPUT:
3 15

~ 3+4* 5/2*8%2

   3+20/2*8%2
   
   3+10*8%2
   
   3+80%2
   
   3+0
   
   3~
   
~ 3+4/2*5+8%3

  3+2*5+2
  
  3+10+2
  
  13+2
  
  15~

~~ +,- have same precedence 

~~ *,/,% have same precedence

~~ precedence(*,/,%) > precedence(+,-)
