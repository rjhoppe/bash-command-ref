Using xargs without specifying an operator will default to echo.
EX:
```
ls * | xargs
```
Validate a command before running it and make sure it is safe.
EX:
```
find -maxdepth 1 -type f -print0 | xargs -0 echo rm
```
By putting an 'echo' in front of the rm, you will see exactly what the command will delete
when you remove the echo.

Run flake8 (Python linter) on a series of filtered Python files:
```
git ls-files ---'*.py' | grep testing | xargs flake8
```
Do run the previous commands in parallel use this:
```
git ls-files ---'*.py' | grep testing | xargs -t -P 5 -n 2 flake8
```
'P' defines the number of processes to use in xargs and
'n' defines how to split up the processes

