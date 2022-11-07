##   CS2400 - PRINCIPLES OF PROGRAMMING LANGUAGE-1

###### -BY TEAM 15

#### Introduction:

A programming language is a formal language comprising a set of instructions that produce various kinds of output. This write-up mainly focuses on language overview, paradigm, general goal, syntax, libraries and input/output based examples. Now, Let’s dive through the language.

#### Name and Origin of our programming Language:
 The name of this programming language is termed as ‘gmat’ since it is created to solve the complex geometry(‘g’) problems in mathematics(‘mat’).So is the name ‘gmat’! The origin of developing this specific language is the complexity of the mathematics involved in solving geometric problems.

#### gmat Language Overview:

gmat language is designed for 2D geometry problem-solving(extension to general problem solving). This language’s main focus is to solve complex geometry problems with ease. Enhanced data types, advanced mathematical operations and functions are specifically designed to suit the needs of the mathematicians.

In python, all the libraries are already loaded by default and so is the lesser execution speed, since while solving the operations it goes all over the unnecessary library files. But here in gmat, only the required library files are included while executing the program. On the other hand, the libraries in gmat support object-oriented programming, unlike c. In addition to that, gmat contains some predefined algorithms which are very much useful rather than building up the required algorithm from the scratch.

 We can extend this notion of our programming language to implement even 3D geometry apart from plane geometry. For example, computer imaging is used nowadays for creating animations, video games, designing, etc. They are all created using geometric concepts. Also, geometry is used in the mapping. Mapping is an essential element in professions such as surveying, navigation, and astronomy. So, later on, gmat will help in designing such features as well.

#### The General Goal of gmat Language:

It is an expressive and versatile language. Its syntax aims to be concise so that users can easily understand how to use it. It is a user-friendly language, unlike many other programming languages. It is used for writing all algorithms similarly used in C, C++. In addition to that, it has libraries which makes it more computational friendly.
    Its main purpose is to write algorithms for solving 2D geometry problems including conics. It is useful to solve computational problems with ease. In addition to that, it gives us good visualization by plotting corresponding figures. It is also helpful in solving and finding roots of polynomial equations.

#### Programming paradigm:
Based on its features, gmat language is a multi-paradigm. It is object-oriented, functional and also procedural.
	gmat language contains object-oriented programming inspired by Cpp. This deals with stuff like data, members, objects and data hiding features rather than bare logic and functions. Classes and objects are present in gmat language similar to the CPP oops. gmat language is imperative when it comes to finding the roots, solving the complex 2D geometry like conics and is declarative when it comes to object-oriented.  
     2D geometry analysis is made easy to the user by adding imperative libraries based on the respective classes of the shapes. All the conics which are used in gmat language are expressed in a general equation given by
    ax^2 + 2hxy + by^2 + 2gx + 2fy + c = 0

#### File extension:
gmat program file extension - .gm
#### Libraries included:
io.LIB - Library for input and output

geo.LIB - Library for geometric functions

plotG.LIB - Library for plotting

and also many other libraries are included like in c,CPP.

#### “Hello world” example and a brief explanation of syntax:

```js
~~helloworld.gm
~~hello world program

add_lib :+ io.LIB     ~add_lib is to include the library
                       while io.LIB is the required library for           
                       input and output~

main::_num             ~function ‘main’ with no arguments and with return
                       type‘_num’. ’_num’ is a data specifier which takes any real value~    

     write(“hello world\n”)   ~ printing “hello world” ~

     return 0
```

A gmat program consists of different functions and variables. A function contains statements that specify the computing operations to be done and variables store values used during the computation.
The above example has a function called ‘main’. Unlike this main function, any other functions can be named in any way we like.
Our gmat program starts executing from this main function. So, every program must have a main function.
Usually, the main function calls other functions to perform its job.
Now, coming to the example, the program starts with ‘add_lib :+ io.LIB’ which tells the compiler to include input and output library in the gmat program.
(There should be no gap between :,+)
A comment is a programmer-readable explanation or annotation in the source code of a computer program.

```js
In gmat program, for comments:‘~~single line comment’
                              ‘~ multi line comment~’
```

Next,’main::_num’ indicates that the main function is defined with no arguments and return type ‘_num’.(In general, the function prototype in gmat is ”function name:arguments:return type”).Since, there are no arguments for the main function, it is left empty.

_num is the datatype in gmat which takes input as any real number irrespective of the decimals and size of the number.
In gmat, a function gets started after leaving Tab space and ends when the Tab space is removed or any value is returned.
(Tab space is mandatory for start of function and must be removed at the end of function)
      Next, the write function is called with the argument “hello world”. ‘write’ is a library function in io.LIB, it prints out the output required. In this case,the string between the quotes.Therefore, the statement ‘write(“hello world\n”)’ prints out ‘hello world\n’.

newline character-’\n’, is used to signify the end of a line of text and start a new one.Unlike c,cpp, in gmat, there is no need of any line termination character like ‘;’.If the given program successfully executes, then it will return ‘0’.

#### Link to example folder:
https://github.com/IITH-POPL1/language-manual-iith15/tree/main/Example%20code%20files


#### CRITICS :
Unlike Python, You need to include the libraries as per requirement to ensure your code works without errors. For now, only 2D geometry problems could be solved limited to two coordinate system.
