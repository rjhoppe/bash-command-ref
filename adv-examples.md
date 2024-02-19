Some advanced examples of cmds you can run from the shell

Fuzzy find any cmd in your system and pull up its manual
```
compgen -c | fzf | xargs man
```

Create an alias for a frequent cmd
```
alias fman="[your full cmd]"
```
Example:
```
alias fman="compgen -c | fzf | xargs man"
```
Don't forget to add this to your bashrc or zrc file for enduring, global usage!


