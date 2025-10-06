# Using Branches & Submitting PRs
When developing for production, we want to refine our code before sharing it. Using GitHub branches lets us do this while keeping version control. It is also how developers typically collaborate.

```{figure} ../figures/github/1-branches.png
---
name: branches-illustration
width: 80%
---
Image by Candace Savonnen (from the book by [The Johns Hopkins Data Science Lab](https://jhudatascience.org/Adv_Reproducibility_in_Cancer_Informatics/using-version-control-with-github.html)).
```

In this section, you'll learn how to create and use a branch, and how to sync this with the main by submitting a *Pull Request* (PR):
```{figure} ../figures/github/pr-illustration.png
---
name: branches-illustration
width: 80%
---
From a book by [The Johns Hopkins Data Science Lab](https://jhudatascience.org/Adv_Reproducibility_in_Cancer_Informatics/using-version-control-with-github.html).
```



```{warning}
This is a bit more "advanced" and not necessarily needed for your own projects, but it can give a lot of peace of mind to work with branches!
```

## Create a Branch
While you can do this via the terminal, I usually just do this on GitHub:
```{figure} ../figures/github/2-branches.png
---
name: branches-view
width: 80%
---
```

Press the "New Branch" button:
```{figure} ../figures/github/3-branches.png
---
name: branches-new
width: 70%
---
```

Give your branch a name (1) and press the green button (2):
```{figure} ../figures/github/4-branches.png
---
name: branches-illustration
width: 70%
---
```

## Using the Branch!
In Coder Python, navigate to your repository `my-repo`:
```
cd nlp/my-repo
```

To get your remotely created branch on your local UCloud repo, pull this change:
```bash
git pull
```

It should say:
```{figure} ../figures/github/5-branches.png
---
name: branches-pull
width: 70%
---
```

Now you can switch to your branch by typing:
```bash
git checkout class4
```

You are ready to work on your branch if the terminal looks like this:
```{figure} ../figures/github/6-branches.png
---
name: branches-switch
width: 70%
---
```

:::{admonition} HANDS-ON
:class: red
Add a change to your README following the [Push & Pull](003_push_and_pull.md) tutorial before proceeding to the next section!
:::


## Submit a Pull Request
When you are done working on you branch and you want to push your changes to `main`, navigate to your repository on GitHub and press "Compare & Pull Request":
```{figure} ../figures/github/7-branches.png
---
name: branches-compare-pr
width: 70%
---
```

Write an appropriate title for your PR and a description of your changes:
```{figure} ../figures/github/8-branches.png
---
name: branches-write-pr
width: 70%
---
```

GitHub automatically checks for merge conflicts. If no issues are found, you can click "Merge pull request" (1) to add your changes to `main`.
```{figure} ../figures/github/9-branches.png
---
name: branches-merge-pr
width: 100%
---
```
There are also useful functions for continued development & collaboration *before* merging:
- Add another user as a reviewer (2) that will look through the code (and recommend it for a PR).
- Review all commits and changed files (3, 4)
- You or a reviewer can add comments to discuss and revise !

As long as you have not pressed "merge" (1), you continue updating your branch and this PR. If a reviewer suggests changes, simply keep refining your work until the branch is ready to merge!

### After the PR: Managing Your Branch
Once your PR is merged, you can either update the branch to continue working on it or delete it (and create a new one for the "next" feature).

#### Updating the Branch
After your PR is merged, your branch will show as “1 commit behind main” because it has not yet registered the merge.

To update it, run the following commands in your terminal while on the branch:
```bash
git pull origin main   # pull latest changes from main
git push               # push to branch to sync with main
```

### Deleting the Branch
You can also just delete the branch (often what is done!). View all branches (1):
```{figure} ../figures/github/2-branches.png
---
name: branches-view
width: 70%
---
```

Press delete: 
```{figure} ../figures/github/10-branches.png
---
name: branches-view
width: 80%
---
```