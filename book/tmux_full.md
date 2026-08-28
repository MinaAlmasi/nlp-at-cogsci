# Tmux (Run Code in the Background)
During your time at CogSci, you may write or encounter code that takes a *long* time to run. Instead of leaving a Python script open all night, you can use `tmux`, a terminal multiplexer that lets you manage multiple terminal sessions. 

With `tmux`, you can start a process on UCloud and safely close your computer while it continues running (as long as you have put enough hours on your job!).

> Good idea to read and go through the [Python Script](python_scripts.md) tutorial first!

## Start a `tmux` session
Let's say you *really* want to print this indefinite loop for a *long* time:
```python
i = 0
while True:
    print(i)
    i += 1
```
But you also want to do other things. Instead of running the .py script from the [previous page](python_scripts.md#stopping-the-code) directly in your terminal, let's open a tmux session:
```bash
tmux new -s <INSERT_NAME>
```

E.g.,
```bash
tmux new -s test
```

This will look as such:
```{figure} figures/tmux/1-tmux.png
---
name: tmux session
```


You can now run your main script from last time:
```{figure} figures/tmux/2-tmux.png
---
name: script-with-infinite-loop
width: 80%
```
With the command `python nlp/src/class4.py`. It should go crazy:
```{figure} figures/tmux/3-tmux.png
---
name: terminal-running-infinite-loop
```

```{warning}
Things to keep in mind:
- You can have multiple tmux sessions, but too many can slow down your system depending on what you are running.
    - It can still be useful to keep certain tasks, like pushing to GitHub, in the main terminal while scripts run in a tmux session.
- Don't open a tmux within a tmux!
```

## Exit a `tmux` session:
Depending on what you want to do, there are ways to exit a tmux terminal session:

### Exit WITHOUT Closing
While in the `tmux` terminal, type: `CTRL-B D` in the following order:
1. Press down **CRTL** and **B** at the same time
2. Let go of **both** keys
3. Press **D** shortly after

### Exit AND Close
1. If you are running a script, stop the script by doing  `CTRL + C`
2. Write `exit` in the `tmux` terminal

## Access an Existing Session
If you exited your tmux session without closing it, but need to open it again, write: 
```bash
tmux a -t <INSERT_NAME>
```

e.g., 
```bash
tmux a -t test
```

## List All Running Tmux Sessions
Need to get an overview of all your open sessions? Type:
```bash 
tmux ls
```



