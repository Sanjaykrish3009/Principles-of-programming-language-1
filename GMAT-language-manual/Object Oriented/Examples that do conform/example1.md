## ***Example 1***

```js
add_library :+ io.LIB 
add_library :+ geo.LIB 

class comparestrings
      private:
            _str a,b 

      public:
        comparestrings::
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
        

main :: _num
        ~~ class is created with default constructor
        comparestrings comparision1:"this example ","is to demostrate classes"
        

    comparestrings xyz



        comparision1.write_string


        ~~class is being created 
        comparestrings comparision2
        ~~using functions in the class to use other functions
        comparision2.injectstrings("this is ","second example")
        comparision2.compare:
        comparision2.write_string:
```

output:
this example is to demonstrate classes
this is  is the greater string
this is second example

~~private: cant be accessed outside the class
~~public: can be accessed outside class 




