**For Windows**
---
Install:
1. Compiler: Cygwin
2. IDE: Codeblocks (free)/ VS code

---
**Installing Cygwin**
You need to install GNU Gcc compiler, make and gdb debugger from https://www.cygwin.com/install.html

` Note: While installing cygwin, on select packages, change View to Full and check mark on bin of gcc-core, gdb and make package.`

Also, ADD ENVIRONMENT VARIABLE PATH on My Computer to C:\cygwin64\bin (if you install on by deafult path).

TO CHECK, If Cygwin is properly installed and added on Environment Variable.
Type `cygcheck -c cygwin` on Command Prompt.

TO CHECK, If gcc is installed ?
Type `gcc --version` on Command Prompt.

**Install CODE::Blocks**
Download Link: https://www.codeblocks.org/downloads/binaries
Normally, install the code blocks.

After installation, it should automatically detect the GCC Compiler. If not, in Settings>> Compilers>>Toolchain executables:
- Compiler's installation directory should be :`C:\cygwin64`
- C Compiler, C++ compiler, and linker for dynamic file should be `gcc.exe` from cywin (C:\cygwin64\bin\) directory.

Also, check for debugger:
It is on Settings>>Debuggers>Default. It's 'Executable Path' should be: `C:\cygwin64\bin\gdb.exe`

**Install VS Code (Optional)**
Install VS Code and also install C/C++ Extension Published by Microsoft.
