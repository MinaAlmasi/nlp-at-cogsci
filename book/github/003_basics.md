# Push & Pull
On UCloud, let's try to add something to the `README.md` on our new `my_-epo`:

```{figure} ../figures/github/6-git-readme.png
---
name: readme
width: 100%
---
```
As you may notice, any change you make is marked with the green bar (and the entire file is marked `M`)

## Push in the Terminal
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

### Add Files
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
### Commit Message
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

### Push!
If it is your first time that you commit on UCloud, you might be asked to state "who you are". See the previous tutorial for how to do this! If you have configured GitHub on UCloud, you can write: 
```bash
git push
```


## Push in the Interface
