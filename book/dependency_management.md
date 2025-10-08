# Dependencies & Setup Script
Now that we have a virtual environment with the required packages, we can reliably reproduce our code on UCloud each time we open a run!

However, to ensure others (and our future selfs!) can do the same without issues, proper dependency management is essential!

```{figure} /figures/dependency_management/python-dep-management-larger.png
---
name: dep-illustration
width: 80%
---
AI-generated, modified by me!
```

This involves creating a `requirements.txt`!

:::{admonition} What about `pyproject.toml` ? 
:class: tip, dropdown
Some projects may not include a `requirements.txt` and instead use a `pyproject.toml`. This format is more flexible and can be generated with tools like [uv](virtual_environments/003_alternatives.md).  

For this course, however, we will stick to using `requirements.txt`.
:::

## Requirements.txt 
As a simple way to save the package versions, you can create a `requirements.txt` that has the package name and version on each line:
```txt
numpy==1.26.4
```

First, activate your environment:
```
source .venv/bin/activate
```

Then, to get version and package information manually, in the terminal, you can type: 
```bash
pip list | grep numpy   
```
`pip list` alone gives you ALL packages whereas the pipe + command `| grep numpy` ensures you only print the packages that you are interested in. 

Then you can create a `requirements.txt` and add `numpy==1.26.4` (or whatever your command said) as a line in the file.

:::{important}
Manually creating a `requirements.txt` gives you full control, but you might accidentally leave out some packages you use.  
- To avoid issues, you should try to re-install your venv + requirements.txt in a diff. folder or machine and see if all your code works with your install setup!

We usually avoid saving the entire `pip list` because `requirements.txt` should include only the packages you explicitly import, not all their dependencies.
:::

### Other ways to create `requirements.txt`?
While creating this book, I found the package [pigar](https://github.com/damnever/pigar) for automatically generating a `requirements.txt`. 

First activate your `venv` in the terminal:
```bash
source .venv/bin/activate 
```

Then install `pigar`:
```bash
pip install pigar
```

Navigate to the directory where your code is e.g., `nlp/nbs`:
```bash
cd nlp/nbs
```

Get `pigar` to do the work:
```bash
pigar generate
```

:::{important}
This is the first time I use pigar, and I think it did quite well, but I would *always* recommend checking the `requirements.txt`:
- Add any packages that are missing or remove weird ones added that you did not import
- To avoid issues, you should try to re-install your venv + requirements.txt in a diff. folder or machine and see if all your code works with your install setup!
:::


## Setup Script
When sharing our code, we do not include the `venv` itself. Instead, we provide instructions for setting it up, including the `requirements.txt`.  

This is usually saved as a `setup.sh` script and might look like:

```
#!/bin/bash

# create virtual environment
python3 -m venv .venv

# activate virtual environment 
source .venv/bin/activate

echo -e "[INFO:] Installing necessary requirements..."

# install reqs
python3 -m pip install -r requirements.txt

# deactivate env 
deactivate

echo -e "[INFO:] Setup complete!"
```