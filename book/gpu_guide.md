# Using GPUs on UCloud
This page contains an overview of how to use GPUs for UCloud. GPU stands for graphical processing unit and they are especially useful for running large language models (and gaming!). 

:::{important} 
Our GPU resources are generally sparse, so please use them wisely. I have written a "Do's and Don'ts", but if in doubt, ask me!

**IF you plan on using GPUs for the exam**, come talk to me and I'll see what I can do.
:::

## Setup (Once)
So far, you have been using CPUs via [SDU](https://docs.cloud.sdu.dk/guide/resources-products.html#drawing-deic-interactive-hpc-sdu-k8s). However, our GPU resources are located on [AAU](https://docs.cloud.sdu.dk/guide/resources-products.html#drawing-deic-interactive-hpc-aau-k8s). You can distinguish by the logos beside the machine names:

```{figure} /figures/gpu-guide/logos.png
---
name: sdu-aau
width: 50%
---
```

The problem is that we **cannot** directly access our current folder `nlp` from SDU on AAU servers. This means that **we have to do setup again**. 

### What You Need to Do
Go to our workspace and try to start a Coder Python run, then select an AAU CPU: 
```{figure} /figures/gpu-guide/AAU-gpu.png
---
name: aau-gpu
width: 100%
---
```

Then, go to **[Class Setup](../book/class_setup.md)** and repeat the guide. That is, you need to create a new `nlp` folder in your AAU member files and mount the new `resources` AAU drive. 

Start the AAU CPU run andrepeat the [virtual environment](../book/virtual_environments.md) setup. Install `pandas` as start. **Then close the CPU run when you are done** !

:::{admonition} HINT
:class: tip
In UCloud (or coder Python), you can drag files from your computer to AAU. So you can work on SDU and then move files to AAU. This is ideal as we don't have many CPU hours on AAU.
:::


## Which Machine to Pick? 
Now tgat tiy re


## GPU Do's and Don'ts