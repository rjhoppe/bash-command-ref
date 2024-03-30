## Config Info

These were configured using a alias.reg file to load the env values from an alias.bat file.

More info on how to do that in Windows 10 here: https://www.randonomicon.com/windows/2020/02/28/windows-cmd-aliases.html

This is what my alias.reg file looks like:

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Command Processor]
"CompletionChar"=dword:00000009
"DefaultColor"=dword:00000000
"EnableExtensions"=dword:00000001
"PathCompletionChar"=dword:00000009
"AutoRun"="C:\\Users\\MyUserName\\Desktop\\alias.bat"
```

And this is my alias.bat file:
```
doskey ls=dir
doskey pyp=cd Documents/Python_Practice/
doskey gop=cd Documents/Go_Practice/
doskey jsp=cd Documents/JavaScript_Practice/
doskey jsxp=cd Documents/React/
doskey tsxp=cd Documents/React/TypeScript/
```

## Shortcut Reference

For Python
```
pyp
```
  
For Typescript
```
tsxp
```
  
For JS
```
jsp
```

For Go
```
gop
```

For React
```
jsxp
```
