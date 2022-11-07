###  ***Example 2***

* There is a difference between multiple and multilevel Inheritance

```js
add_library :+ io.LIB

class a
    protected:
        a::
            write("constructer of a is called.\n")
class b
    private:
        b:_num:
            write("constructer of b is called.\n")
class c: protected a,private b
    public:
        c::
            write("constructer of c is called.\n")

main::_num
    c varaible

```
* only protected and pubic members can be accessed from base class in the derive class objects. It would give you an error if you write constructers in private of a base class.
