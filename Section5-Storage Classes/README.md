## Storge classes
---
C provides four storage classes:
- auto
- register
- extern 
- static

The Four storage class specifiers can be split into two storage durations
- automatic storage duration
- static strorage duration

---

#### Auto Storge class (local variables):
Keyword auto is used to declare auto storage duration (created in a block e.g. function or in loop), exists while the block is active and destroyed when the block is exited.
The keyword auto is not used while declaring, because it doesnot provide compabality while writing C/C++ programs and has different meaning in C++. 

```
Syntax:
storage_class var_data var_name;

Example Code:
auto double x,y;
```
---
### External Storage class ( global variabales)
External variable or global variables are stored outside the function and can be accessed any where in the program(also, in another file of same program.)
```
Synatx: 
storage_class var_data var_name;

Example Code:
// declare anywhere (int moveNumber=1;) in other file and use 
// in using the given using the variable.

extern int moveNumber;

// keyword is 'extern' not 'external'
// we should not initalize the variable in extern keyword declaration place.
```

Similary, extern specifier can be used on to the  functions. It can be called anywhere from a file and where it doesnot need to be defined in a header file. It is by default property of an variable and doesnot need to use keyword.

```
Example Code:

extern double foo(double x){.....}

```

---
### Static Storage Class
It can be used on local and global variables, as well as functions. 
When the applied to local variable it instructs the compiler to keep the variable in existence during the life-time of the program.

When applied to global variables, the static modifier causes that variable's scope to be restricted to the file in which it is declared.

When applied to functions, the static function can be called only from within the same file as the function appears.

```
Example code:

static int count=0; \\static variable

```

Stack variables are allocated memory on the heap, not on the stack.

Static variables should not be declared inside a structure as C compiler requires entire structure elements to be placed together (as memory allocation for structure members should be contiguous).

---
### Register Storage class
A process register(CPU Register) is one of a small set of data holding places that are part of the computer processor( holds instruction, a storage address or any kind of data).

It is used to define local variable that should be stored in a register instead of RAM(register variables are much faster than variables stored in Memory(RAM)). It cannot be used in as global variable.

Same functionality as the Auto Variables, the variables stored in a register has a maximum size equal to register size.

You cannot obtain the address of a register variabels using pointers.

```
Example code:

register int x;

```