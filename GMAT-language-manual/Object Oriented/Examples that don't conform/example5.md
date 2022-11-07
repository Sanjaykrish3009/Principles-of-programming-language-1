### ***notconfirm-Example-4***

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
        operater .:complex x:complex
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
    c3 = c1.c2
    c3.print::
    return 0
```
* the above code even though completely similar to the confirm method example-4 it wont work.
* Operater overloading can't be done on unary and tertiary operarters.
* Ooperater overloading cant be done on operaters like :, ::, .,
* binary operaters are a better choice when it comes to operater overloading in gmat
* operater overloading makes it easy for the one who uses these classes, but it makes harder for the class developer.
