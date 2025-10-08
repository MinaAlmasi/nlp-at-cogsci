# Integrate with UCloud
The first time you try push anything to GitHub on UCloud, you will get a "Please tell me who you are" message ... follow the tutorial below to make UCloud & GitHub friends!


## Passing your Credentials
Let's tell GitHub who you are :)

### In the Terminal
Type in your credentials:
```bash 
git config --global user.email "you@example-com"
git config --global user.name  "Your Name"
```
By credentials, please replace the `"you@example.com"` with the mail connected to you GitHub and `"Your Name"` with your GitHub username (you don't need to write it in quotations).

### UCloud Hack: Mount a Bash Script with Credentials!
To avoid having to type in your credentials each time, you can save a bash (`.sh`) script with your information and mount it for each Ucloud run:

Create the `github_setup.sh` in Coder Python. I saved mine to my `nlp` folder:

```{figure} ../figures/github/github_sh.png
---
name: github_sh
width: 80%
---
```

Next time you open a UCloud run, look for the "Optional Parameters" and press "Use" on the `Initialization`:

```{figure} ../figures/github/init.png
---
name: init
width: 100%
---
```

Find your newly created `github_setup.sh` and mount it, just as you would for a folder!

```{figure} ../figures/github/init_with_sh.png
---
name: init
width: 100%
---
```

When you submit your job, this script will run while it is starting up! (in principle, you can add whatever you want to this script).


## Pushing the First Time
The first time that you try to push (see next tutorial), you will be met with a pop-up where you need to press "allow":
```{figure} ../figures/github/1-ucloud-git-extension.png
---
name: ucloud-git-extension
width: 80%
---
```

You will then see a code. Here, you should press "Copy & Continue to Github":

```{figure} ../figures/github/2-ucloud-git-code.png
---
name: git-code
width: 80%
---
```

Press "Open":
```{figure} ../figures/github/3-ucloud-git-open.png
---
name: git-open
width: 80%
---
```

You'll be prompted to sign in, press "continue":

```{figure} ../figures/github/4-ucloud-git-activate.png
---
name: git-activate
width: 80%
---
```

Paste your code and press "continue" again!
```{figure} ../figures/github/5-ucloud-git-paste-code.png
---
name: git-paste-code
width: 80%
---
```

Press the green button again ;)
```{figure} ../figures/github/6-ucloud-git-authorize.png
---
name: git-authorize
width: 80%
---
```

Now comes a step where we might differ - but you need to confirm access somehow:
```{figure} ../figures/github/7-ucloud-git-confirm-access.png
---
name: git-confirm
width: 80%
---
```

When you have confirmed access, you can now push any changes you made :))
```{figure} ../figures/github/8-ucloud-git-congrats.png
---
name: git-congrats
width: 80%
---
```