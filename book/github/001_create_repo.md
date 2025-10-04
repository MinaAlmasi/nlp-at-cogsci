# Create & Clone a Repo
Let's begin a new repository for a code project that is in Python. 

## Create a New Repo
Go to [github.com](https://github.com/). On the main page, there should be a green "new" button that you should press:

```{figure} ../figures/github/1-git-new-repo.png
---
name: new-repo
width: 90%
---
```

Give your repository a meaningful name and optionally a short description! For this tutorial, we'll call it `my-repo`:


```{figure} ../figures/github/2-git-name-repo.png
---
name: name-repo
width: 90%
---
```
:::{admonition} How to choose a good name for my repo?
:class: dropdown, tip
Name your repository in a way that connects to your project while remaining meaningful. You can use lowercase, hyphens, or capitalization. I don't believe in strict rules. Here are some examples from existing repositories:
- [EuroEval](https://github.com/EuroEval/EuroEval)
- [mteb](https://github.com/embeddings-benchmark/mteb)
- [meta-agents-research-environments](https://github.com/facebookresearch/meta-agents-research-environments)

Remember that you can always change the name later ;)
:::

### Configuration
Select "add readme" (1), choose the Python `.gitignore` template (2). 
```{figure} ../figures/github/3-git-config-repo.png
---
name: config-repo
width: 90%
---
```
We won't choose a license (3) today (and it is not needed for this course), but it can be useful for 

:::{admonition} What is `.gitignore`? & Tip for Mac!
:class: tip, dropdown
`.gitignore` tracks what should **not** be pushed to Git. The Python template makes sure that your `.venv` and other weird Python artefacts don't get pushed.

Exclude folders by writing the folder name and a star in your `.gitignore`:
```
data/*
```

Or just specific files:
```
data/super_large_datafile.csv
```

**TIP:** While we mostly use UCloud, if you happen to use your own Mac at some point, please add `.DS_Store` to your `.gitignore`!
```
.DS_Store
```
:::

### Ready to Create!
Scroll to the end and press the green button to launch your git adventure!
```{figure} ../figures/github/4-git-create-repo.png
---
name: create-repo
width: 90%
---
```

## Clone your Repo
To start working on UCloud with your repository, press the green code button (1) and copy the url (2):
```{figure} ../figures/github/5-git-clone-repo.png
---
name: clone-repo
width: 90%
---
```

### In Coder Python
Open a terminal and navigate to your `nlp` folder (or somewhere else where you would like to place your repository):
```bash
cd nlp
```

Write the command below with your pasted url:
```bash
git clone URL 
```

(For my case it would be `git clone https://github.com/MinaAlmasi/my-repo.git`)

