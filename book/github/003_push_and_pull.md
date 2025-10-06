# Push & Pull
On UCloud, let's try to add something to the `README.md` on our new `my-repo`:

```{figure} ../figures/github/6-git-readme.png
---
name: readme
width: 100%
---
```
As you may notice, any change you make is marked with the green bar (and the entire file is marked `M`)

## In the Terminal
I highly recommend you get learn this workflow in the terminal as Coder Python / Visual Studio Code can sometimes be buggy (or you might end up getting a job where you need to do it in the terminal!). 

However, I'll also provide a guide on how to do this in the interface below this one!

### Push Changes
Navigate to your repository. If you cloned to `nlp`, from `work` it should be:
```bash
cd nlp/my-repo
```

To see if there are any changes, type:
```bash
git status
```

If you made the same change as I, then it should say:
```{figure} ../figures/github/7-git-status.png
---
name: git-status
width: 80%
---
```

As a first step in pushing, we need to `add` any files that we want to "commit" at the same time (think of this as "registering" the files together): 

#### Add Files
To add the README.md specifically, we type:
```bash
git add README.md 
```

If have several files and want to add them all at the same time:
```bash
git add . 
```

If we type `git status`, it should look like this:
```{figure} ../figures/github/8-git-status-added.png
---
name: git-status-added
width: 70%
---
```
#### Commit Message
Our next step is to add a commit message which describes the changes we made:
```bash
git commit -m "Add sentence to README"
```

It should look like this:
```{figure} ../figures/github/9-git-commit.png
---
name: git-status
width: 80%
---
```

#### Ready to Push!
If it is your first time that you commit on UCloud, you might be asked to state "who you are". See the previous tutorial for how to do this! If you have configured GitHub on UCloud, you can write: 
```bash
git push
```

### Pull
To pull any changes from your current branch, you simply write 
```
git pull 
```

If you did not modify a file locally that was already changed remotely, this will go smoothly. If not, you might get a `merge conflict`. See how to deal with those [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line).

## Coder Python Interface
You can also do the whole workflow in Coder Python!

### Push
Click on the "+" to add a change:
```{figure} ../figures/github/10-git-coder-python.png
---
name: git-coder-python-star
width: 80%
---
```

Write your commit in the message box and press COMMIT
```{figure} ../figures/github/11-git-coder-python.png
---
name: git-coder-python-msg
width: 80%
---
```

Press the "Sync Changes" button:
```{figure} ../figures/github/12-git-coder-python.png
---
name: git-coder-sync
width: 80%
---
```

### Pull
Super simple, press pull on the drop-down:
```{figure} ../figures/github/13-git-coder-python.png
---
name: git-coder-python-pull
width: 80%
---
```
