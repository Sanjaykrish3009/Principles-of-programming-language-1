## ***Example 2***

* functions - help in breaking large programs into smaller tasks

```js
func:_str expression _num degree:_str roots
    _poly Eq:n
    Eq = [expression]
return Eq 
```

~~ arguments must be seperated by commas!!
~~ _str roots is incorrect, it represents a character whereas the ouput is roots of polynomial stored in an array of numbers.
~~ variable 'n' is defined in main function; It cant be accessed in the function. scope of varaible 'n' is from the placed it is declared to end of main function.


