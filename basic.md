# bash-command-ref
A list of some helpful commands to remember when I write bash

Reverse search for previous bash commands in your terminal history.
```
Ctrl+R
```

Run "Fixed Command" (fc) after running an incorrect command to open up the previous command in a text editor.
```
fc
^xe
```

Pronounced "bang bang" (!!), this command will take the previous command and substitute it for the "!!"
A good example of when to use this is when you forget to preface a command with sudo.
```
!!
sudo !!
```

This command takes the last part of the previous command and substitute it into the current command
```
!$
```
An example of how this could be used, clone to a particular local directory and then cd into that directory:
```
git clone git@github.come/rjhoppe/reponame local_directory
cd !$
```

Similar to !$ this command lets you cycle through the last parts of previous commands
```
ALT+.
```

This command produces a Tab character in your terminal
```
CTRL+V
```
Wraps text output at a certain character limit --spaces command will respect word boundaries
```
[command that outputs string] | fold -w 40
[command that outputs string] | fold -w 40 --spaces
```
This command will kill programs / commands that maybe can't be killed by CTRL+C. This should be used as a last resort and isn't always safe.
```
CTRL+\
```
