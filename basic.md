# bash-command-ref
A list of some helpful commands to remember when I write bash

Shows full path to current directory
```
pwd
```

Lets you view longer text files in a scrollable format
```
less [file name]
```

Remove all text/commands currently in your shell
```
Ctrl+U
```

Reverse search for previous bash commands in your terminal history.
```
Ctrl+R
```

Move current process to the background
```
Ctrl+Z
```
Use 'fg' to bring that same process back to the foreground
```
fg
```

Open up your current cmd in a text editor to make editing easier
```
Ctrl+X Ctrl+E
```
Save your changes to see your updates in the shell

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

Push and pop directories off the stack and allow Linux to keep track of your directory stack, so that you can effectively 'pop' out of it when
you need to. This is particularly handy when you are writing bash scripts
Instead of:
```
cd ../../../
```
Try this
```
pushd foo
```
And then pop off the stack when you're finished:
```
popd
```

Learn more about a particular bash cmd
```
man [cmd]
```
Or try
```
tldr [cmd]
```

Sort data in a file (will default to alphabetical)
```
sort [file name]
```
Or use the -n argument for 'numeric'
```
sort -n [file name]
```

When looking at logs use this cmd to automatically see new log entries (lines) as they are created
```
tail -f log
```

Use 'fzf' to activate the 'fuzzy finder'
```
fzf
```

List all the cmds you can run (this can take a couple of seconds to run)
```
compgen -c | less
```

View the last run cmds in your bash history
```
tail ~/.bash_history
```

Clear all input in your bash terminal
```
CTRL+U
```

A more detailed ls output
```
ls -lsah
```

Move or rename a file in place
EX:
```
mv file.txt newname-txt
```

Zip files with tar and compress the zipped file
Note: files are not automatically compressed with tar by default
EX:
```
tar -zcf archive.tar.gz file1.txt file2.txt folder1
```

Unpack a zipped file to a destination
Notice we swapped c for x in the flags. This is because we went from creating to extracting. 
And then the -C is just giving it a destination folder to extract it.
EX:
```
mkdir destination-folder
tar -xzf archive.tar.gz -C destination-folder/
```
