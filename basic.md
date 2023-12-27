# bash-command-ref
A list of some helpful commands to remember when I write bash

Remove all text/commands currently in your shell
```
Ctrl+U
```

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

Search for a particular command or command keyword in your Linux CLI history
```
history | grep [command keywork, i.e. 'networks']
```

Difference between ';', '&&', and '||' when chaining multiple bash commands (&& is most likely what you are looking for)
```
; - Both commands run
&& - When first command passes, then onto the next command
|| - When first command fails, then go onto the next command
```

Seach for a particular file name in all directories
```
find . -name [file name]
find . -name main.py
```

Search for a particular file name pattern in a particular directory
```
sudo find [directory] -name *[pattern]
sudo find /etc -name *.conf
```

Search for file names with particular permissions associated with it
```
find . -perm 664
```

Search for particular directories or subdirectories
```
find /etc -type d
find /etc -type d -name [directory name] 
```

Configure command aliases to run your own shorthand for more verbose bash comamnds (need to run the source command to refresh the .bashrc file)
```
sudo nano ~/.bashrc
alias c='clear'
alias sysboost='sudo apt update && sudo apt upgrade -y && sudo apt autoclean'
source ~/.bashrc
```

Example of how you might use grep to search for a file or directory name prefix
```
ls | grep '^[search term]'
```

Fix command - this will trigger an editor pop-up that will allow you to edit your typo'd command
Quit the editor to run the fc'd command
```
fc
```
