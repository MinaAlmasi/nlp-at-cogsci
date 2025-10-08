# Installation
See the step-by-step on how to install a virtual environment using `venv` in UCloud!

## Steps
Note that steps 1-3 only need to be done **once** for every virtual environment you install.

> If you don't plan to use Jupyter Notebooks, step 3 is not needed.

### 1. Change working directory 
In the terminal, navigate to where your code is present:
```bash
cd nlp
```

:::{admonition} How do I open a Terminal in Coder Python?
:class: tip, dropdown

:::

### 2. Create virtual environment
Type in the terminal:
```bash
python -m venv .venv 
```
```{admonition} Naming your environment
:class: dropdown, tip
In principle, you can call your environment `MyAwesomeEnv`, but the standard practice is to call it `.venv` (or `.env`). This also adheres to GitHub's `.gitignore` template, making it less likely that you will push your environment to Git.
```

(venv-step3)=
### 3. Install `ipykernel` and attach your environment
Do these additional steps to use Jupyter Notebooks with your new `.venv`:

Activate your environment (see [next page](#activate-your-environment) for explanation)
```bash
source .venv/bin/activate
```

Install `ipykernel`:
```bash
pip install ipykernel
```

Navigate to the folder where your notebooks are located
```bash
cd nbs
```

Attach your `.venv`:
```bash
python3 -m ipykernel install --user --name=.venv 
```

## Removing your venv?
Not anything you should do now, but if you want to get rid of your virtual environment (e.g., to reinstall everything), you simply need to remove the folder by typing (while in `cd nlp`):
```bash 
rm -rf .venv
```