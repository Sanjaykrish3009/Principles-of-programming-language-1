## ***Example 4***


```js
add_library :+ io.LIB


class demonstrate

    private:

    public:
        demonstrate::

        destruct demonstrate::
            log::            //may cause an exception to be thrown
            throw exception

try::
    demonstrate exceptionclass1
    demonstrate exceptionclass2

catch:exception:
    write("exception caught\n")
```

~~In the code above, if exception occurs twice, such as during the destruction of both objects, the catch statement is never executed. Because there are two exceptions in parallel, no matter whether they are of the same type or different type the gmat does not know how to handle it and calls a terminate function which results in termination of a program’s execution.

So never allow exceptions to leave destructors.

