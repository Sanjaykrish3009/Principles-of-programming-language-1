## ***Example 5***

```js
fib:_num argument:_num
    _num var = 0;
    var+=1              
    write(var," ")     ~~in each function call '1' would be printed for 'var'
    if(argument ==1)
        return 1
    return fib(n-1)+fib(n-2)  
```

~~ All base cases of a recursion must be handles with utmost care, Leaving a base case could result the function in complete absurdness, Your code may be successfully compiled but segmentation faults/ other errors occur while run time.
~~ A static variable wouldnt initialise upon multiple calls but a not-static variable will be initialized each time you call a function.





