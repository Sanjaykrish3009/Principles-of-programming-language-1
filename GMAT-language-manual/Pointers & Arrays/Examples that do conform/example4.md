## ***Example 4***

* string pointers 

```js
add_librabry:+io.LIB
add_librabry:+str.LIB

main::_num
_str *A ={"hello world!","This is gmat","Popl project"}
~~A is a string pointer like array of strings
~~It stores value dynamically
~Initialization must be in the format same as above i.e, A={"string1","string2",...."stringn"}~
strcpy(A[3],A[1])
~A[3] can also be accessed even the Initialization is upto A[2]~
write("2nd string : ",)
write("\nenter the 5th string: ")
read(A[4])
if : strcmp(A[1],A[3]) == 0
  write("\nstrings 2nd and 4th strings are same")
else
  write("\nstrings 2nd and 4th are not equal") 

strcat(A[2],A[3])
write("\n3rd string is : ",A[2])
return 0
```


OUTPUT:

2nd string : This is gmat 

enter the 5th string: Gmat programming language

strings 2nd and 4th strings are same

3rd string is : Popl projecthello world!


