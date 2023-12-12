# tmux-command-ref
A list of some helpful commands when using tmux

Create a new tmux tab
```
Ctrl+B + C
```

Switch to a particular tmux session (you will know this works when the * switches to the tab you specified)
```
Ctrl+B [tab #]
```

Detach current tmux session
```
Ctrl+B + D
```

Reatach tmux session
```
Ctrl+B + A
```

Split sessions into two panes
```
Ctrl+B + %
```
Or
```
tmux split-window
tmux split-window -hf
```

Switch between windows
```
Ctrl+B + Arrow Left/Right
```
NOTE: Press Ctrl+B then release then press either arrow key

Change size of split windows
```
Ctrl+B + Arrow Left/Right
```

Add another window split on your right side
```
Ctrl+B + '
```


Kill current tmux session
```
tmux kill-session
```
