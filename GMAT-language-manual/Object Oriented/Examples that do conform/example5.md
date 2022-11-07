### ***Example  4***

* operater overloading
* gmat allows you to have more than one defination for an operater in the same scope

```js
add_library :+ io.LIB

class complex
    private:
        _num real,imag
    public:
        complex::
        complex:_num ireal,_num iimag:
            real = ireal
            imag = iimag
        operater +:complex x:complex
            complex temp
            temp.real = real + x.real
            temp.imag = imag + x.imag
            return temp

        print::
            write(real,"+",imag,"i\n")

main::_num
    complex c1(2,3)
    complex c2(3,4)

    complex c3
    c3 = c1+c2
    c3.print::
    return 0
```
OUTPUT:

5+7i
