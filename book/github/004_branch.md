# Using Branches & Submitting PRs
When developing for production, we want to refine our code before sharing it. Using GitHub branches lets us do this while keeping version control. It is also how developers typically collaborate.

```{figure} ../figures/github/1-branches.png
---
name: branches-illustration
width: 80%

Image by Candace Savonnen (from the book by [The Johns Hopkins Data Science Lab](https://jhudatascience.org/Adv_Reproducibility_in_Cancer_Informatics/using-version-control-with-github.html)).
---
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


## Submit a PR 
When you are done working on your, navigate to your branch on GitHub:


### What to do with the branch after this?
You can either delete it via GitHub:
