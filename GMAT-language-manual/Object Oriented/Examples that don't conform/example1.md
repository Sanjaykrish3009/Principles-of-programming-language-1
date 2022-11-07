## ***Example 1***

~~DO NOT CONFIRMS....:

```js
class comparestrings
      private:
            _str a,b 

      public:
            comparestrings:x,y:void
                a = x,b = y
        
            void injectstrings:x,y:void
                a = x,b = y
        
            compare::
                  if:a>b
                  write(a,"is greater string","\n")
                  else:
                  write(b,"is greater string","\n")
            
        write_string:: 
            write(a,b,"\n")
main::_num
    comparestrings variable:

    variable.inject:"qwerty","asdfg"
    variable.compare:
```

~~ Above class has only one constructer which takes two strings as input
~~ So while initialising that class variables you need to give two strings as input, if not you will have an error saying :no matching constructer!.    





