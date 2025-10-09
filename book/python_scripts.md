# Python Scripts
So far, we have worked exclusively in notebooks, which are useful for learning experimenting with small code snippets. For a more professional workflow, using scripts is often preferable.

```{figure} figures/python_scripts/nbs_to_src.png
---
name: notebook to script
width: 80%
---
AI-generated, borrowed from [Zaher (2025)](https://medium.com/@rabailzaheer/can-i-convert-ipynb-to-py-107c877f678a).
```



This page gives you a brief intro to this, but this is also something that will come naturally to you as you practice coding in Python :).

```{warning}
You don't have to use scripts for the exam if you feel more comfortable with notebooks, but I encourage you to practice using scripts !
```

## The "Main" Idea ;)
Instead of creating a `.ipynb`, you need to create a `.py`: 
```{figure} figures/python_scripts/1-py-scripts.png
---
name: py scripts
---
```

To begin, you normally import any relevant packages at the top (as you do with notebooks):
```{figure} figures/python_scripts/2-py-scripts.png
---
name: py scripts packages
---
```

Any workflow you would normally do in a notebook, you could do here:
```{figure} figures/python_scripts/3-py-scripts.png
---
name: py scripts worfklow
---
```

However, common practice would actually be to denote what you are running under this syntax:
```{figure} figures/python_scripts/4-py-scripts.png
---
name: py scripts name_main
---
```


> This above basically signals "if this python script is run as the main thing, run these lines of code"

Even more ideally, you would write a `main()` function:
```{figure} figures/python_scripts/5-py-scripts.png
---
name: py scripts main_fn
width: 80%
```

This lets you define functions outside of `main()` or even import your own from other scripts and then use them within `main()`.
```{figure} figures/python_scripts/6-py-scripts.png
---
name: py scripts name_fn
```

## Running the Code
To run the script, you need to locate where it is placed:
```bash
cd nlp/src
```

And run the code as such:
```bash
python class4.py
```

You could also run without changing paths:
```bash
python nlp/src/class4.py
```

### Package Imports?
If you are running code without having installed the right packages, you have two options:
1. Install the imported package(s) in the terminal (`pip install pandas`)
2. Activate your virtual environment with the packages installed (see [venv tutorials](virtual_environments.md)) or install them after activating it!

If we go with option 2, the full workflow is thus:
```bash
source .venv/bin/activate

python nlp/src/class4.py
```

## Stopping the Code
Sometimes, you might run something that takes a long time or is buggy in some way. Let's say you really wanted to print a bunch of numbers:
```python
i = 0
while True:
    print(i)
    i += 1
```
The code above will literally run FOREVER. Press `CTLR + C` to stop it!