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

List all available Kubernetes pods and then select the desired pod to pass over to kubectl to describe it
```
kubectl get pods -A --no-headers | fzf | awk `{print $2, $1}' | xargs -n 2 sh -c 'kubectl describe pod $0 -n $1'
```

Find the biggest files in a directory and return the path
```
du -ah . | sort -hr | head -n 10
```
du = finds file size <br />
ah argument = reverse order <br />
hr argument = human readable <br />

History of most used cmds, sorted by most to least used
```
history | awk '{print $2}' | sort | uniq -c | sort -nr | head -10
```

Redirect stdout to one place and stderror to another place
EX:
```
ls -lsash 1> ls-stdout.txt 2> ls-stderror.txt
```

Check shell type
```
cat /etc/issue
```

Use the test cmd to run various tests (i.e. is A = B?, etc.)
Learn about how you can use the cmd by running:
```
man test
```
