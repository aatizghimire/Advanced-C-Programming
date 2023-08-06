###Different VS CODE Configuration Instructions for project Setup
---
`Note: 1. The tags like these <Name>, can be changed as you requirement.`
*Also, **create a New Folder** to setup project and do these configuration.*

**Configure Compiler**
- Go to VS Code>>View>>Command Palette.
- Type and go to "C/C++ : Edit Configuration UI"

- Inside this configuration:
    - Set Compiler path to :`C:\cygwin64\bin\gcc.exe`
    - Set Intellisense: "`gcc-x64`" and exit.

**Configure Build**
- Go to VS Code>>View>>Command Palette.
- Type and go to "Tasks: Configure Default Build Task"
- Create tasks.json file from template >> Others.
- In 'tasks.json' change label : `<your-label>`, and add 
```"args":[ "-g","-o","<helloworld>","<helloworld.c>"], "group":{"kind": "build", "isDefault": True} ```

*The main source file should match in helloworld.c*

**Configure Debugger**
- Go to VS Code>>View>>Command Palette.
- Type and go to "Debug: Open launch.json".
- Select "`C++ :GDB/LLDB`"
- Change:`"program" :$workspacefolder\<executablename.exe> `, `"stopAtEntry": True`, `"miDebuggerPath":'C:\cygwin64\bin\gdb.exe'`

**Configure Terminal as Bash**
- Go to VS Code>>View>>Command Palette.
- Type and go to "Prefrences: Open settings (JSON)". 
- On settings.json, Add `"terminal.integrated.shell.windows": 'C:\\cgwin64\\bin\\bash.exe'` after file.associations.

After configuration, `Ctrl + Shift + V` , to run the task. It will sucessfully compile the code, by running task. Check the directory (`ls` command in terminal) to find executable file and run by `./<executable-name.exe>`.

### Or
Use "coderunner" extension in VS Code to do this task.