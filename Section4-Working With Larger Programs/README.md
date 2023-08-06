### Building Project With multiple files

---

**Create a Project to run multiple files**
1. Create a Project in Code Blocks.
2. Create a `other.h` header file from New>>Files>>C/C++ headers. Add these lines:

```
#ifndef OTHER_H_INCLUDED 
#define OTHER_H_INCLUDED

int getfavoritenumber(void);

#endif // OTHER_H_INCLUDED`
```
3. Create a `other.c` source file from New>>Files>>C/C++ source. Add these lines:
```
#include "other.h"

int getfavoritenumber(void){
    return 3;
}
```

4. In main.c add these lines:
```
#include <stdio.h>
#include "other.h"

int main(void)
{
    printf("%d\n",getfavoritenumber());
    return 0;
}

```
5. Build and Run.

```
Note: If a Reference error comes, while building the project, go to 
Projects>>Properties>>Build Target>> build target files
check on "other.h, other.c,etc." both on "debug and release" 
```

### In VS Code
Same technique is applied but while compiling multiple files, command is:
`$ gcc *.c -o main`
or
`$ gcc main.c other.c -o main`

OR 
in tasks.json file (inside args add)

``<helloworld.c>, <add-other-c-files.c> ``


### If you want to compile individiual code
```$ gcc -c main.c```
then, to get executable from object file
```$ gcc main.o -o main```

---
### Make - C (File utility tool)
This tool is used to compile large  C projects.

---
#### Static vs Extern Variable
Static Variable keyword lets us limit the visibility of things within the same file, while Extern Variable let the see variable from everywhere.

---
### Using Header file effectively.
Use modular coding to divide big code into smaller chunks and join by using including header file.

---
### Heap and Stack Memory Allocation
- Stack (LIFO) is created when function runs, it is temporary and automatically freed when the function is dead (easier and faster). While, Heap is a dynamic memory have larger memory than stack, and persistant, needed to be made free, needed to create a big array or struct (slow while reading and writing).

- In heap, programmer has to allocate and manage memory using calloc(), realloc(), malloc() and free().

- Stack has limitation on memory size and it can overflow during recursion called stack overflow.