# ***APPENDIX A***

## A.1.Introduction

The manual so-called describes the language 'gmat' in detail. 'gmat' is an efficient, powerful and yet easy to use programming language from general-purpose to high-level use. The focus of this reference manual is on the language itself, not the implementation of it. The language constructs are described in the text and with examples rather than formally specified. This is to make the manual more readable. While coming to the prerequisites, this manual is written assumed that the reader has a minimal idea in aspects of a programming language such as control flow, data types and object-oriented. The core of the manual consists of a series of chapters on various topics. The topics have been chosen by the complexity, importance and frequency of their use in programming.

## A.2.Lexical Conventions
Any gmat program consists of one or more translation units stored in files. It is then translated into several phases for better performance. The Initial phases of the program will do low-level lexical transformations, carry out directives(libraries) introduced by the lines beginning with the ‘add_library :+’ , and then perform macro definition and expansion. Later, the program gets to sequence of tokens after the preprocessing of (A.12) is completed.

## A.2.1 Tokens
In gmat programs, each word and punctuation is referred as a token. The compiler breaks a program into the smallest possible units and proceeds to the various stages of the compilation, which is called token. Tokens are the smallest building block or smallest unit of a program.

In gmat, there are five classes of tokens: identifiers, keywords, constants, operators, and other separators. Blanks, horizontal and vertical tabs, newlines, and comments as described below (collectively, ''white space'') are ignored except as they separate tokens.

Note: Except for horizontal tab spaces, they are used to differentiate the block of codes or scope used in the indentation are percieved by the compiler otherwise are ignored.  

## A.2.2 Comments
A comment is an explanation of source code of the program for better understanding and readability of the user. At run-time, a comment is ignored by the compiler. There are two types of comments in gmat:

* Single-line comments, indicated by “~~comments”
* Multi-line comments, indicated by “~comments ~”

## A.2.3 Identifiers

In gmat programming, each program element is known as an identifier. They are used for naming of variables, functions, array etc. where ever necessary.
The first character of an identifier must be an alphabet; the underscore ‘_’is also counted as a letter. Uppercase and lowercase letters are considered as different letters. Identifiers may have any length, Internal identifiers include preprocessor macro names and all other names that do not have external linkage. Identifiers with external linkage are more restricted

## A.2.4 keywords
Keywords are predefined, reserved words in gmat and each of which is associated with specific features. These words should not be used as identifiers.
```js
_num      _string    _polygon     _poly    _conic    struct    auto     union
break     else       switch       case     typedef   return    enum     register
volatile  const      continue     for      void      default   goto     extern
sizeof    do         if           static   while     _point  
```

## A.2.5 Constants
#### Real number constants

A real number constant consists of an integer part, a decimal part, a fraction part. The integer and fraction parts both consist of a sequence of digits. Either the integer part, or the fraction part (not both) may be missing; the decimal part may or may not be present. The type is determined by the suffix ‘_num’

#### String constants

A string consists of group of characters, which are enclosed in “ ”. The type is determined by the suffix ‘_string’

## A.3. Syntax Notation
In this manual, syntactic notation is given in the following way:

*	literal words and characters in typewriter style.
*	Programming part is highlighted in boxed structures.

## A.4.1: Identifiers

Identifiers refer to the names of functions; classes; variables; enumeration constants and objects..etc. The Identifier's name begins with an underscore or lower/upper case letters. An identifier can't be named after a keyword.

Object or variable identifiers are defined only under their scope. Each object identifier has a region of the program where it is known(that is the scope of the object). The object gets destroyed as its scope is exited. Along with scope, Objects also have a linkage that determines whether the same name in different scope refers to the same object.
Automatic objects are local to their scope or block of code. If an object is not declared with static-specifier or if declared with auto-specifier is considered an automatic variable. Static objects storing methods are different compared to the automatic objects, this enables them to store their values even after exiting the block. The latter is declared by adding a keyword static in front of its declaration, The linkage used here would enable them to continue with their previously-stored values when the block of code is called again. static objects declared in a translational unit have internal linkage. The objects declared globally along with function declarations are always static, this gives them external linkage.

## A.4.2: Types of Objects

The most fundamental types we have are _num and _str Types. _str type variables have a definite memory to store each character variables. _num, unlike _str, provides memory based on the value stored in the object. This ensures appropriate memory usage but there do exist limits to the range of values that can be stored in _num type variables. The io.LIB libraries also contain the ranges in MIN__num and MAX__num. In general, it provides a space as that of a single precision float point. If the input variable overflows the limits of MAX__num, the corresponding modulo value is produced.

void type specifies an empty set of values.

Constructed from these fundamental types, we also have a class of derived types like :

* arrays of objects of given types
* functions ;structures ;classes
* pointers of an object of given types
* graphs of object of given Types
* polygons; polynomials; conics of objects(arrays of expression in general) of given types

## A.4.3: Type Qualifiers

Type Qualifiers add additional information to the type of objects. There are two such Qualifiers constant(const object) and volatile(volatile object). Const objects are unmutable, trying to change them would give a runtime error or undefined behavior if you use pointers to address to change it.
Further discussion of Qualifiers is done in section_A.8.

## A.5.Objects and Lvalues

An object is simply a name for the storage allocated and Lvalue is something that refers to the name, while identifiers are names given to different entities such as classes, functions, variables. Declarations often establish a necessary mapping between objects and identifiers. For mapping identifiers and objects, we must have at least two attributes namely storage class and data type.

The range of objects that can be declared includes:
*	 variables
*	 functions
*  data types
*	 arrays, strings
*	 classes
*	 preprocessor macros

while coming to Lvalues, it is an object locator as mentioned above, an expression that designates an object. For sample example, an Lvalue expression is *ptr, where ptr here refers to any non-null pointer dealing expression. Simply a modifiable Lvalue is an identifier or expression that relates an object that can be accessed and legally changed in memory. For example, a constant pointer to a constant is not a modifiable Lvalue, since the dereferenced value cannot change. At last, if num1 and num2 are two different non-constant number identifiers with proper allocation of memory, both of them can be modified lvalues, which eventually suggests that num1 and num2 can be assigned and changed in an expression.

## A.6.1 : Pointers and Numbers 
An expression of numerical type may be added to or subtracted from a pointer; in such a case the numerical expression is converted as specified in the discussion of the addition operator.

Two pointers to objects of the same type, in the same array, may be subtracted; the result is converted to an number as specified in the discussion of the subtraction operator. An numerical constant expression with value 0, or such an expression cast to type void *, may be converted, by a cast, by assignment, or by comparison, to a pointer of any type. This produces a null pointer that is equal to another null pointer of the same type, but unequal to any pointer to a function or object.

Certain other conversions involving pointers are permitted, but have implementation-defined aspects. They must be specified by an explicit type-conversion operator, or cast. A pointer may be converted to an numerical type large enough to hold it; the required size is implementation-dependent. The mapping function is also implementation-dependent.

A pointer to one type may be converted to a pointer to another type. The resulting pointer may cause addressing exceptions if the subject pointer does not refer to an object suitably aligned in storage. It is guaranteed that a pointer to an object may be converted to a pointer to an object whose type requires less or equally strict storage alignment and back again without change; the notion of "alignment" is implementation-dependent, but objects of the char types have least strict alignment requirements. A pointer may also be converted to type void * and back again without change.

A pointer may be converted to another pointer whose type is the same except for the addition or removal of qualifiers of the object type to which the pointer refers. If qualifiers are added, the new pointer is equivalent to the old except for restrictions implied by the new qualifiers. If qualifiers are removed, operations on the underlying object remain subject to the qualifiers in its actual declaration.

Finally, a pointer to a function may be converted to a pointer to another function type. Calling the function specified by the converted pointer is implementation-dependent; however, if the
converted pointer is reconverted to its original type, the result is identical to the original pointer.

## A.6.2 : Void
The (nonexistent) value of a void object may not be used in any way, and neither explicit nor implicit conversion to any non-void type may be applied. Because a void expression denotes a
nonexistent value, such an expression may be used only where the value is not required. An expression may be converted to type void by a cast. For example, a void cast documents the discarding of the value of a function call used as an expression statement.

## A.6.3 : Pointers to Void
Any pointer to an object may be converted to type void * without loss of information. If the result is converted back to the original pointer type, the original pointer is recovered. which generally require an explicit cast, pointers may be assigned to and from pointers of type void *, and may be compared with them.
This interpretation of void * pointers is new; previously, char * pointers played the role of generic pointer. The ANSI standard specifically blesses the meeting of void * pointers with object pointers in assignments and relationals, while requiring explicit casts for other pointer mixtures.

## A.7.Expressions

Expressions in 'gmat' has atleast one operand and zero or more operators, same as the other programming languages have. Operands are objects such as constants, variables, function calls and return types (data types).

	For example:
		898
		84.23 + 66.5
		tangent(56r)
		( 45 * ( 2 + 3)/ (2 - 6) )

These are all expressions in 'gmat', where in the fourth example, it is evaluated according to the predecence rules mentioned in the chapter***, while the outermost parenthesis are completely avoidable. An operator specifies an operation to be performed on its operands. operators may have one, two or three operands, depending on the operator.

## A.7.1.pointer conversion
Pointers serve a very good purpose in supporting languages,so does here. pointer have the address stored of a particular memory block. One can use address operator '&' for dereferencing a pointer to get memory address of object stored.

	For example:
		_num var = 5.5
		_num* ptr_var = &var
It's not necessary to use the dereferencing operator to obtain the address of a function. Function pointers are not compatible, in the sense we cannot expect to store the address of a function into a data type pointer, then copy into another function pointer and we can call it successfully, but its not a reliable technique in 'gmat'.
```js
_num var = 5.5, number
_num* ptr

ptr = &var ~~ the _num pointer ptr now have the memory address of var
number = *ptr ~~the value of var is copied into number
```  

Dereferencing a pointer which is not initialized may give unwanted output. So it is better to avoid dereferencing of uninitialized pointers.


## A.7.2.Primary expressions
An expression enclosed in parenthesis is called a primary expression. Simply, primary expressions are the building blocks of complex expressions. They may be string literals, variables, names qualified by the kwywords or so.

	Examples:
		100
		'c'  
		"string literal"
		operator overload '+'
		( var + 1 )
		functionfoo::

  These are all considered as primary expressions in 'gmat'.

## A.7.3.Postfix expressions

Postfix expressions consist of expressions in which postfix operators follow a primary expression. The postfix operators are listed in the following table. The operators groups from left to right.

	some of the notations:
		function call operator ::
		subscript operator []
		type-conversion operator type_name:
		member accessor in class ->(mostly) or .(also)
		postfix increment operation ++
		postfix decrement operation --

possible syntax for postfix expressions in 'gmat'

    postfix-expression[expression]
    postfix-expression(expression-list) simple-type-name(expression-list)
    postfix-expression.name
    postfix-expression->name
    postfix-expression++ 	
    postfix-expression--

### A.7.3.1 Array references
A postfix expression followed by an expression in square brackets is a postfix expression for denoting the subscripted array reference. Either one of the two must have a pointer pointing to some data type. Subsequently suggesting that the other one must be an integer type.
```js
		let array[5] = {0,1.4,2,3.6,4}
		array[3] = 3.6
```    
where array is simply a pointer pointing to the _num data type and the integer is
present in the subscript notation. It eventually denotes that it is simply returning *(array + 3) memory block.

### A.7.3.2 Functioncalls
Well we know, with the general notion of programming knowledge, that function is something that we need to have in our code to avoid any code duplication and for better readability. Let's have a look in 'gmat' function calls,

when a function is called, these following two things primarily happens. firstly, all actual arguements are evaluated, there is no particular order in which these arguments are evaluated, but all are evaluated and all effects are completed prior to entry in the function. secondly each formal arguement is initialized with corresponding actual arguments in the expression list. And then it executes the rest.

Example:
```js
	suppose fprime is a function which takes _num as input and gives _num as output
	_num prime = 7
	_num var = fprime:prime
```    

This is the function call syntax for functions in 'gmat'
And also there are many more inbuilt libraries for plotting and solving the geometry problems with an ease, the function calling is same though in every context.

### A.7.3.3	classes reference
This comes under the member access in the class where we need to call function or access the class members. In general the access is done with (dot). operator for normal members and (arrow)-> operator for pointer variables.

let us create a class :-
```js    
		class memberaccess
			private:
				_num privatenumber
			public:
				_num publicnumber
				_num* ptr_to_number
```
and after once they are initialized, we can access members as memberaccess.publicnumber , memberaccess->ptr_to_number another form of *(memberaccess).ptr_to_number. But the access to private members can be done only within the class without using access operators.

### A.7.3.4 Postfix incrementation/decrementation:
A postfix expression followed by double + or - operator comes under this section. It increments or decrements according to the operator given and type of the operand. If it is a number type, then it increments or decrements it by 1 or so based on the condition and if it is a pointer type, then it gives the memory address of incremented or decremented reference address.

Example:

		a++ is postfix increment expression which suggests that a = a+1
		*ptr-- is postfix decement expression which returs the previous memory block of ptr.

### A.7.4 Type Casting
casting, generally referred as type casting is used to make an expression to be a specific data type. Type cast in 'gmat' generally consists of datatype followed by colon. Also casting is allowed only to the scalar types, like number type, string literal or a pointer type.

	cast-expression = (type_name)tobe_castedexpression
	Example:
		_num var = 10
		_str string = _str:var
		now string contains a string literal "10"
		similary a pointer from one datatype to other datatype also can be successfully casted in 'gmat'.

## A.7.5 Multiplicative operators
The multiplicative operators *,/ and % functions from left to right.
The operands of * and / must have arithmetic type, generally takes any numerical value except the '0' for division, while % operand must have integral type. _num make sures all are used correctly whenever necessary. And these follows standard rules of mathematics while solving the operations. However, we can load these operators too.

## A.7.6 Additive operators
The additive operators + and - also functions from left to right. If the operands are of numerical type, usual arithmetic operations are performed. These operators also wrok on pointers. Same as the arithmetic operations these serve the purpose of pointer arithmetic where we can get the incremented or decremented memory address as we fill the instruction.

## A.7.7 Shift operators
The shift operators << and >> both must have integers as arguments in the expression if these are considered as functions, as operands if considered as operators. Generally we use left shift operator << to shift first operands bits to the left, the second operator denotes the number of bit places to shift. similarly we use the right shift operator >> to shift the first operands bits to the right. Bits which shifts out gets discarded and added are generally 0. If Negative or value greater than bitwidth is used as second operand, it would give unwanted results.

## A.7.8 Relational operators
The relative operators have left to right associativity. Both operators must be of arithmetic or pointer type.

	operators:
		less than <
		greater than >
		less than or equal to <=
		greater than or equal to >=

It comes with a bit tricky in terms of using these operators on pointers. If two pointers point to elements of the same array or to element beyond the array, the pointer object with higher subscript is treated higher. If class type is union, then pointers to different data members in the same union are treated equal. And also these operators are to be used only when pointers are of same type.

## A.7.9 Equality operators
The two most used operators == and != are coined under equality operators because of the work they do. == is equality operator and != is not equal operator.
If both the operands are equal then == returns true and != returns false and vice versa.

## A.7.10 Bitwise AND operator
The bitwise AND operator '&' compares each bit of first operand to each bit of the second operand. As it does from standards, if both the bits are 1 then the resultant bit is 1 and subsequently all the other leads the resultant bit to be 0. Both the operands for this operator must be integers.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 & var2

## A.7.11 Bitwise OR operator
### A.7.11.1 Exclusive
The bitwise exclusive OR operator ^ compares each bit of first operand and corresponding bit of second operand. If the bits of either one of the operand is 1 then resultant bit is 1 and else the resultant bit is set to zero. Both the operands must have iteger type.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 ^ var2

### A.7.11.2 Inclusive
The bitwise inclusive OR operator | compares each bit of its first operand to corresponding bit of second operand. If either bit is 1 , resultant bit is set to 1 , else bit is set to 0. Also both the operands must have integer type.

	_num var1 = 2
	_num var2 = 3
	_num var3 = var1 | var2

## A.7.12 Logical AND operator
The logical and operator && returs 1 if both operands are 1 and else results in 0. The operands doesn't need to be of same type. They have left to right associativity. This operator is confined to boolean, number or pointer type.

## A.7.13 Logical OR operator
The logical or operator || returns 1 if either one of the operands are 1 and else results in 0. Similarly this operand doesn't need to be of same type. It's left to right associative. This operator is also confined to boolean, number or pointer type.

## A.7.14 Conditional operators
The conditional operator is a ternary operator ()?():() The first operand here is converted to integer 1 or 0. If first operator is 1 then second operand is set to evaluated else the third operand is set to evaluated. Which suggests that only one of second or third operand is evaluated. It have right to left associativity.

	For example:
	_num i = 10.5 , j = 27.33
	write(i>j?i:j,"is greater than the other")

## A.7.15 Assignement operators
The assignment operators store a value in the object specified by the left operand. simple and compound assignments divide these operators. Simple assignment is the one which the value of second operand is stored in the object of first operand. Where the compund assignment is performed without storing.

		= storing the value
		*= multiply the firstoperand to second and stored in first
		/= divide the firstoperand to second and stored in first
	 	%= gives the modulus of first operand and is stored in first
	 	+= adds the first operand , sceond operand and is stored in first
	 	-= substracts the first operand , sceond operand and is stored in first
	 	<<== leftshifts the operand by the value and hets stored in first operand
	 	>>== rightshifts the operand by the value and hets stored in first operand
	 	&= stores the bitwise and of two operands in first operand
	 	^= stores the bitwise exclusive or of two operands in first operand.
	 	|= stores the bitwise inclusive or of two operands in first operand.
```js    
	Example
		_num a = 1 , b = 2 , c = 3 , d = 4
		a += b
		b -= c
		c *= d
		d /= c
		c %= d
		a |= d
		these all comes under assignment operators.
```		
## A.7.16 Comma operator
The two operands seperated by comma gets evaluated left to right. Commas can be used as separators in function araguments and function calling.

	_num var1 = 10.5 , var2 = 0.23 , var3 = 666
	var1 = var2,var3
	write(var1)
	var1 = (var2,var3)
	write(var1)

It yields different results.

## A.7.17 Constant expressions
Constant expressions are the ones which are not subjected to change. If we are supposed to have a data literal which shouldn’t change its value or contents at any point of time in execution of program, this constant expressions are made for you.

    Example:
    const _num variable = 10
    this variable never changes with course of time.
    Similarly const can be used before any data type. Contents in const type remains intact.

## A.8 Declarations
Declarations specify the interpretation given to each identifier; they do not necessarily reserve storage associated with the identifier.  A declaration must have at least one declarator, or its type specifier must declare a structure tag, a union tag, or the members of an enumeration; empty declarations are not permitted (Declarators will be discussed later (Par.A.8.4); they contain the names being declared)

Declarations have the form declaration:
“declaration-specifiers declarator-list”
* The declarators in the declarator-list contain the identifiers being declared.
*  The declaration-specifiers consist of a sequence of type and storage class specifiers.

## A.8.1 Specifiers

### i) Storage Class Specifiers
#### 1) auto
The auto specifiers may be used inside the functions and give the objects (which are declared) automatic storage class, and these type of declarations serve as definitions and cause storage to be reserved
#### 2) register
A register declaration is equivalent to an auto declaration, but now, the declared objects will be accessed more frequently. only certain types are eligible; the restrictions are based on implementation. However, if an object is declared register, the unary ‘&’ operator may not be applied to it, explicitly or implicitly.
#### 3) static
The static specifier gives the object which are declared, static storage class, and can be used either inside or outside functions. This specifier causes storage to be allocated inside the function, and serves as a definition; for its effect outside a function.
#### 4) extern
The extern specifier specifies that the storage for the declared objects is defined elsewhere; for its effects outside a function.
#### 5) typedef
The typedef specifier does not reserve storage and is called a storage class specifier only for syntactic convenience  

At most one storage class specifier may be given in a declaration. If none is given, these rules are used: objects declared inside a function are taken to be auto; functions declared within a function are taken to be extern; objects and functions declared outside a function are taken to be static, with external linkage.

### ii) Type Specifiers
The type-specifiers are:
  *   void
  *   _num
  *   _string
  *   _point
  *   _polygon
  *   _poly
  *   _conic
  *   struct-or-union-specifier
  *   enum-specifier
  *   typedef-name  

Types may also be qualified, to indicate special properties of the objects being declared.

type-qualifier:
  *  const
  *  volatile

Type qualifiers may appear with any type specifier.
 A const object may be initialized, but not thereafter assigned to.
There are no implementation-dependent semantics for volatile objects.

## A.8.2 Structure and Union Declarations
A structure is an object consisting of a sequence of named members of various types. A union is an object that contains, at different times, any of several members of various types.

Structure and union specifiers have the same form.
A struct has a declaration list, which is a sequence of declarations for the members of the structure or union:

    Example:
      struct Address
	       _num street_No
	       _string street_Name           ~This the declaration list of struct Address~
	       _string city
           struct Address*next

           ~It contains street number, name of the street, name of the city ~
      struct Address k
      struct Address *p
           ~declares k to be a structure of the given sort, and p to be a pointer to a structure of the given sort. ~
      p->street_No
           ~~refers to the ‘street_No’ field of the structure to which p points;
      k.next
           ~~refers to the next pointer of the structure k.

## A.8.3 Enumerations
 Enumerations are unique types with values ranging over a set of named constants called enumerators.

The identifiers in an enumerator list are declared as constants of type _num, and may appear wherever constants are required. If no enumerations with = appear, then the values of the corresponding constants begin at 0 and as the declaration is read from left to right, each constant increase by 1. An enumerator with = gives the associated identifier the value specified; subsequent identifiers continue the progression from the assigned value.

    Example:
    add_library :+ io.LIB
    enum Month{Jan, Feb, Mar, Apr}   ~~Jan=0,Feb=1,Mar=2,Apr=3
    main::_num
	    enum Month x
        x=Mar
        write(x)
        return 0

        OUTPUT: 2
Importantly, Enumerator names must all be distinct from each other and from ordinary variable names, but the values need not be distinct.

## A.8.4 Declarators
A list of declarators appears after a sequence of type and storage class specifiers. Each declarator declares a unique main identifier. The storage class specifiers apply directly to this identifier, but its type depends on the form of its declarator. (see below pointer, array declarators)

#### i)pointer declarators
The declaration of pointer has the following syntax:
“Datatype * identifier”

For example, consider the declaration

_num *ap

Here, ap plays the role of an identifier; the declaration ''_num ap'' would give ap the type '' _num'', but now the actual declaration “_num *ap” gives ap the type `` pointers to _num''

#### ii) array declarators
The declaration of an array has the following syntax:
“Datatype identifier[constant-expression]”

If the constant-expression is present, it must have integral type, and value greater than 0. If the constant expression specifying the bound is missing, the array has an incomplete type.

An array may be constructed from an arithmetic type, from a pointer, from a structure or union, or from another array (to generate a multi-dimensional array)

    Example:
    _num a1[17], *a2[17] ~declares an array of real numbers, an array of pointers to real(_num)   

#### iii) function declarators
In gmat, a function declaration has the syntax of the form:
“FunctionName(identifier) : parameters-list : return-type ;”

The parameter-list specifies the types of the parameters. For a function with no parameters has an empty parameter-list and with return type “void”.

    Example:
    strcpy : _num *dest,  _string source : _num
    ~strcpy is a function returning ‘_num’, with two arguments, the first one is ‘_num’ pointer, second one is a string. ~

## A.8.5 Initialization
When an object is declared, then its declarator may specify an initial value for the identifier being declared.

The initializer is preceded by =, and is either an expression, or a list of initializers nested in braces.

    Example: _num x = 3

#### i)array initialization
For an array, the initializer is a brace-enclosed list of initializers for its members (as shown in the example below). If the array has unknown size, the number of initializers determines the size of the array, and its type becomes complete.
Example: _num x[] = {1,2,3}
If the array has fixed size, the number of initializers may not exceed the number of members of the array; if there are fewer, the trailing members are initialized with 0.  The number of initializers must not be greater than the number of elements to be initialized.

    Example: _num y[3] = {1} ~~array with fixed size
                        ~~only, y[0] is initialised to ‘1’ , and others i.e, y[1],y[2] are initialized to ‘0’
#### ii)pointer or arithmetic type
The initializer for a pointer or an object of arithmetic type is a single expression. The expression is assigned to the object.
That is, to assign a value to an arithmetic or pointer type, use the simple initializer: = expression.

    Example: _num x= 3, _num *p=&x  
#### iii)_point datatype
There are two initializers for a _point datatype enclosed by “[“,”]” this set of brackets as shown below.

    Example: _point P = [-2,3]

#### iv)_polygon datatype
Number of initialisers for _polygon datatype depends on the number of sides of the polygon required.
These initialisers are separated “;” and all are enclosed by “[“,”]” this set of brackets, as shown below.

    Example: _point A= [0,0], B= [0,4], C= [3,0]
                  _polygon Tri = [A; B; C] ~~Tri is a right-angled triangle
#### v)_poly datatype
Number of initialisers for _poly datatype depends on the degree of the polynomial required.
These initialisers are separated “,” and all are enclosed by ‘[‘  , ‘]’ this set of brackets, as shown below.

    Example: _poly Eqn=[1,2,3]
    ~~ The initialisers are coefficients ‘x^n’ in decreasing order of power of x
    ~~Eqn represents the polynomial:  1*x^2 + 2*x + 3


#### vi)_conic datatype
There are six initializers for a _conic datatype enclosed by “(“,”)” this set of brackets and each each initialiser is separated by ‘, ’, and finally, initialising a conic with the help of ‘inject’ function as shown below.

    Example: _conic var.inject(1,0,1,0,0,-9)
      ~conics general equation ax^2+2hxy+by^2+2gx+2fy+c~
      ~Here var is a circle with centre origin and radius 3 ~
#### vii)_string datatype
The initializer for _string datatype is group of characters enclosed by “ ”, as shown below.

    Example: _string Name= “Principles of Programming Language-1”
#### viii)structure or union
The initializer for a structure is either an expression of the same type, or a brace-enclosed list of initializers for its members in order. Unnamed bit-field members are ignored, and are not initialized. If there are fewer initializers in the list than members of the structure, the trailing members are initialized with 0. There may not be more initializers than members.

    Example:
      struct address
	       _num street_No
	       _string street_Name
	       _string city
      struct address My_address= {“12”,” Kandi”,” Hyderabad”}
#### A.8.6 Typedef

Declarations whose storage class specifier is typedef do not declare objects; instead they define identifiers that name types. These identifiers are called typedef names.
A typedef declaration attributes a type to each name among its declarators in the usual way . Thereafter, each such typedef name is syntactically equivalent to a type specifier keyword for the associated type.
A typedef does not introduce new types, only synonyms for types that could be specified in another way.

    Example:
    typedef _num Block
    ~~after the above declaration
    Block b   ~~ It is a legal declaration. The data type of b is _num

## A.9 : Statements

Statements are executed in sequence. Statements are executed for their effect, and do not have values. They fall into several groups.

```js
  statement:
    labeled-statement
    expression-statement
    compound-statement
    selection-statement
    iteration-statement
    jump-statement
```

## A.9.1 : Labeled Statements

Statements may carry label prefixes.
```js
  labeled-statement:
    identifier : statement
    case : constant-expression : statement
    default : statement
```
A label comprising of an identifier declares the identifier. The only use of an identifier label is as a target of "jump". The scope of the identifier is the current function. Since labels have their own name space, they don't meddled with other identifiers and cannot be redeclared. Case names and default labels are utilized with the switch statement. The consistent expression of case must have "numerical type" or "string type". Labels themselves do not alter the flow of control.

## A.9.2 : Expression Statement

expression Statement are in the form
```js
  expression-statement:
    expression
```
Most expression statements are assignments or function calls. All side effects from the expression are completed before the next statement is executed. If the expression is missing, the construction is called a null statement; it is often used to supply an empty body to an iteration statement to place a label.

## A.9.3 : Compound Statement

So that several statements can be used where one is expected, the compound statement (also called "block") is provided. The body of a function definition is a compound statement.
```js
  compound-statement:
    declaration-listopt statement-listopt
  declaration-list:
    declaration
    declaration-list declaration
  statement-list:
    statement
    statement-list statement
```
If an identifier in the declaration-list was in scope outside the block, the outer declaration is suspended within the block, after which it resumes its force. An identifier may be declared only once in the same block. These rules apply to identifiers in the same name space; identifiers in different name spaces are treated as distinct.

Initialization of automatic objects is performed each time the block is entered at the top, and proceeds in the order of the declarators. If a jump into the block is executed, these initializations are not performed. Initialization of static objects are performed only once, before the program begins execution.

## A.9.4 : Selection Statements

Selection statements choose one of several flows of control.
```js
  selection-statement:
   1) if: expression
      statement
   2) if: expression
      statement
      else:
      statement
   3)switch : expression
      statement
```
In both forms of the "if" statement, the expression, which must have arithmetic or pointer type, is evaluated, including all side effects, and if it compares unequal to 0, the first substatement is executed. In the second form, the second substatement is executed if the expression is 0. The "else" ambiguity is resolved by connecting an "else" with the last encountered "else"-less "if" at the same block nesting level.

The "switch" statement causes control to be transferred to one of several statements depending on the value of an expression, which must have "Numerical type" or "string type". The substatement controlled by a "switch" is typically compound. Any statement within the substatement may be labeled with one or more "case" labels. The controlling expression undergoes "numerical or string" promotion, and the case constants are converted to the promoted type. No two of these case constants associated with the same switch may have the same value after conversion. There may also be at most one "default" label associated with a switch. Switches may be nested; a "case" or "default" label is associated with the smallest switch that contains it.

When the "switch" statement is executed, its expression is evaluated, including all side effects, and compared with each case constant. If one of the case constants is equal to the value of the expression, control passes to the statement of the matched "case" label. If no case constant matches the expression, and if there is a "default" label, control passes to the labeled statement.If no case matches, and if there is no "default", then none of the substatements of the swtich is executed. The controlling expression of switch, and the case constants, were required to have "_num type or _str type".

## A.9.5 : Iteration Statements

Iteration statements specify looping.
```js
  iteration-statement:
    1)while: expression
      statement
    2)do
        statement
      while: expression
    3)for:expression1, expression2: expression3:
       statement
```
In the "while and do statements", the substatement is executed repeatedly so long as the value of the expression remains unequal to 0; the expression must have arithmetic or pointer type. With "while", the test, including all side effects from the expression, occurs before each execution of the statement; with do, the test follows each iteration.

In the "for" statement, the first expression is evaluated once, and thus specifies initialization "for" the loop. There is no restriction on its type. The second expression is evaluated after each iteration, and thus specifies a re-initialization "for" the loop. The third expression must have arithmetic or pointer type; it is evaluated before each iteration, and if it becomes equal to 0, the for is terminated.There is no restriction on its type. Side-effects from each expression are completed immediately after its evaluation. If the substatement does not contain continue,a statement
```js
  for: expression1, expression2: expression3:
    statement
is equivalent to
expression1
while: expression3
statement
expression2
```
Any of the three expressions may be dropped. A missing third expression makes the implied test equivalent to testing a non-zero element.

## A.9.6 : Jump statements

Jump statements transfer control unconditionally.
```js
  jump-statement:
    jump identifier
    continue
    break
    return expression
```
In the "jump" statement, the identifier must be a label located in the current function.
Control transfers to the labeled statement.
A continue statement may appear only within an iteration statement. It causes control to pass to the loop-continuation portion of the smallest enclosing such statement. More precisely, within each of the statements
```js
  1)while:....
      .......
      continue
  2)do:....
      .......
      continue
    while:....
  3)for:.....
      .......
      continue
```
a "continue" not contained in a smaller iteration statement is the same as jump continue.

A "break" statement may appear only in an iteration statement or a "switch" statement, and terminates execution of the smallest enclosing such statement; control passes to the statement following the terminated statement.

A function returns to its caller by the "return" statement. When "return" is followed by an expressions, the values is returned to the caller of the function. The expressions is converted, as by assignment, to the type returned by the function in which it appears. There can be two or more return expressions. Flowing off the end of a function is equivalent to a return with no expression. In either case, the returned value is undefined.

```js
function:argumnets:return_1,return_2
    function body
    return x,y
  ~~x,y contain the values to be returned.
  ~~x,y correspond to return_1 and return_2 respectively

main::_num
    _num a,b
    (a,b) = function:arguments:

```

## A.10

The input to the compiler is provided in units(called translational/computational units), each consisting of a sequence of external declarations/ function definitions. These units form the final input to the compiler from which object files are generated. The scope of the external declaration lies till the end of the unit.

```js
  computational unit:
    external declaration:
      function defination
      declarations ...
      computational units:external declarations ...
```

Simply put declaring an object outside of a function is called an external declaration. (the object is declared without being defined). Note that memory allocation is done while defining the object.

## A.10.1 : Function Definations

In gmat function definition format is like this:

The functions Declarater consists of the function identifier and the arguments declaration specifiers and their idenatifiers respectively.
```js
func_identifier:arg_declaration_specifier arg_identifier:func_declarater_specifier
     code of the function program

```
multiple arguments can be provided separated by commas, and similarly, multiple declaration specifiers can be given, an indication that function would return more than one value/object.

A function may return an arithmetic type, a structure, a union, a void, but never an array or another function pointer. The parameters list is the arguments lists along with their declaration specifiers, The parameter list refers to the type, order, and the number of parameters in the function. If no declaration is given for the parameter it is taken to be of _num type. Default parameter initialization is allowed in CPP, it is better to write them at the end of the parameter list.

Note: Functions won't be able to return arrays, but the Solve: Equation functions are defined in the geo.LIB function has the ability to store the final result in an array directly. The type of implementation used here is inspired by lists used in python.

## A.10.2: External Declarations

External declarations are used to specify the characteristics of objects, functions, and other identifiers. External declarations discuss the declaration of functions/objects; it's different from the keyword 'extern'.

External Declarations format/syntax :
```js
func_identifier:arg_declaration_specifier arg_identifier:func_declarater_specifier;
```
Different external declarations may exist for the same identifier only if they agree in both type and linkages, and there should be only one definition for the identifier.
```js
static _num x=2  ~~definition; internal linkage
_num x           ~~tenative definition: gives undefined behavior
                 ~~     since there should be only one definition for an identifier
```
If an external object declaration does not contain an 'extern' specifier then it's called a tentative definition. if no further definition for the object appears then the tentative definitions initialize objects to zero or else they just become redundant declarations. If the static specifier is not used in the object's first declaration then the object is considered under external linkage.
```js
_num x = 10        ~~definition; external linkage  
_num x             ~~tentative definition; becomees a redundant declaration here
extern _num x      ~~extrnal declaration; refers to the earlier defination

_num y             ~~tentative definition; intialised to 0
static _num p      ~~tentaive definition; internal linkage
_num q             ~~external declaration; external linkage

_num z             ~~tentative definition; becomes redundant declaration here
extern _num z =10  ~~external definition
```
```js
static _num x
extern _num x=6  
~~ doesn't throw an error(x gets initialized and declared as extern) but once the extern is defined inside a function it throws an error

static _num y=5
extern _num y
~~ here y is initialized and declared as static and the second line becomes redundant.

static _num z=6
extern _num z=5
~~ throws an error
```
objects with the internal linkage must have the same definitions in its translational unit since they are internally linked objects. objects with the external linkage must have the same definition through out the program.

## A.11

A program need not all be compiled at one time: the source text may be kept in several files containing translation units, and precompiled routines may be loaded from libraries. Communication among the functions of a program may be carried out both through calls and through manipulation of external data.
There are two kinds of scope: first, lexical scope of an identifier which identifier's characteristics are unterstood. second, scope associated with objects and functions which determines the connections between identifiers in compiled translation units.

## A.11.1 : Lexical Scope

The lexical scope of a declaration is the declared name’s range of visibility within its own translation unit.  It begins at the end of the declaration and continues unbroken until an end point that depends on the type of declaration.  For an internal declaration, that point is the end of the containing block.  For a parameter of a function definition, that point is the end of the function.  For an external declaration, that point is the end of the translation unit.  Nested declarations of the same name have overlapping lexical scopes, and each one hides the others that are outside its own block.  A declaration of an object, including the extern keyword, which occurs earlier than the object’s definition in the same source file, commences the lexical scope at the earlier point.

All function definitions are external, since gmat does not allow nested functions.  Therefore, a translation unit consists of external declarations (declarations of objects and functions) and function definitions.

## A.11.2 : linkage

gmat can (and often is) implemented to use different linkage conventions. The most basic reason for that is gmat’s greater emphasis on type checking. A practical reason is that gmats supports overloading, To begin with external decleration for an identifier gives the identifier internal linkage in the event that the "static" specifier is utilized, external linkage otherwise. If a decleration for an identifier inside a block does not incorporate the "extern" specifier, at that point the identifier has no linkage and is one of a kind to the function . In case it does incorporate "extern", and an external statement for is dynamic within the scope encompassing the piece, at that point the identifier has the same linkage as the exernal decleration, and refers to the same object or function; but in case no external decleration is visible, its linkage is external.


## A.12.Preprocessing

Preprocessors ensure that the code is preprocessed(inclusion of files, symbolic preprocessing of equations and conics if required, macro substitution, and conditional compilation) before the compilation starts. The preprocessor directives tell the preprocessor what to do. In gmat preprocessor directives are identified by their names, there is no '#' added at the beginning. add_library, define, ifndef, endif are some of the preprocessor directives in gmat.

## A.12.1: Digraphs and Trigraphs:

Both Digraphs and Trigraphs are omitted in gmat programming implementation. You may enable them by writing separate command lines.
```js
enable:+digraphs
enable:+trigraphs
```
When the above command lines are used compiler replaces the trigraph sequence with the corresponding punctuation character.
```js
Trigraph character     Equivalent             Digraph character   Equivalent
??=                     #                     <:                  [
??/                     \                     :>                  ]
??'                      ^                     <%                  {
??(                     [                     >%                  }
??)                     ]                     %:                  #
??!                     |                     :%                  ##
??<                     {
??>                     }
??-                     $
```
Note: A digraph string or a trigraph string occurring inside a quoted string or character constant shall not be replaced. gmat also poses additional tokens which can be accessed by default. The Trigraphs, Digraphs, and tokens (if present) are converted before the tokenization(refer to A.12.3) begins.

## A.12.2: Macro Definition and Expansion
```js
define identifier(identifier_list) token_sequence

undef identifier  ~~removes the token_sequence(if any) applied to the identifier(if any).
```
A Macro definition consists of a preprocessor directive, an identifier, and the identifier list(optional), and a token-sequence. The identifier list consists of parameters. Wherever the identifier is written, it is replaced by the corresponding token sequence. The parameters list if present is replaced by corresponding arguments in order. If the arguments list doesn't match with the parameters list it throws an error. Multiple Macro definitions for the same identifier throw an error unless they are identical. The token sequence must be written there itself, following the same indentation rules as general codes do.

example:
```js
define list_printer(start,end) while:start<end
                                   write(start," ")
                                   start++
~~ code ...

undef list_printer
```

The operation of Macro differs in presence of two operators # and ##. if a # character occurs then the identifier is replaced by the token-sequence placed inside quotes, and each " and \\ that appear are added with a \\.

## A.12.3: File inclusion

```js
add_library :+ "filename"    
add_library :+ filename      
```
Both the above command lines include the contents of the file identified by the filename into the present source file. If there is no file with the given filename then the program throws an error. The filenames used in the above command lines must not contain characters such as *,',",/,\\,'

The first command-line searches for the files under standard gmat directories. The standard gmat directories can be controlled by the user. The second command line first searches the directory where the current source file exists, and only if the file is not found, it searches through standard directories

## A.12.4: Conditional Compilation

The conditional compilation works similar to an if else-if conditions.
```js
If: expression
Ifdef: identifier
Ifndef: identifier

Elif: expression

Else:

Endif
```
The conditional processing starts with an If: or Ifdef: or Ifndef and is evaluated in order until a non-zero value is found. Only the text following the successful derivative is executed. If no non-zero value is found, the text under Else: is executed. If the identifier is defined as a macro, the macro substitution is done first. The conditional Compilation block is ended by an Endif

## A.12.5: Line control
```js
Line constant "filename"
Line constant
```
makes the compiler to believe that the next source line is given by the integer "constant" written just after the Line derivative. Macros in the line are expanded before it is interpreted.

example:
```js
write(__LINE__," ")
Line 10
write(__LINE__)
```
OUTPUT: 1 10

## A.12.6 Error Generation
```js
Error token-sequence
```
causes the preprocessor to write a diagnostic message that includes token-sequence.
* The functions related to geo.LIB may not return messages here unless the input given doesn't match with the syntax or the input is undefined, These functions are written in functional programming essence, these can't be accessed by the user. Any return of undefined values of these functions is stored as 'nan'(not a number).

## A.12.7: Pragmas
```js
Pragma token_sequence
```
The Pragma directives are used to provide some extra information. If a pragma is not identified, it is ignored.

examples:
```js
Pragma startup token_sequence
~~ before the start of main, the token_sequence is to be executed

Pragma exit token_sequence
~~ before the end of the program, the token sequence is executed
```
## A.12.8 Predefined Macro Names
```js
__DATE__  ~~ contains the date of compilation of source file in string literal form: "mm dd yyyy"
__FILE__  ~~ name of the current source file
__LINE__  ~~ The current line number
__TIME__  ~~ contains the time of compilation in the format: "hh mm ss"
```
Several identifiers are predefined. They can't be redefined again.
