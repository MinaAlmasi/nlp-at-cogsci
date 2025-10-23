# Using GPUs on UCloud
This page contains an overview of how to use GPUs for UCloud. GPU stands for graphics processing unit, and they are especially useful for running large language models (and gaming!). 

:::{important} 
At the moment, GPU resources are sparse. You can use GPUs, but you'll have to use them wisely! See [Best Practices](#best-practice-principles-for-gpu) below.

**IF you plan on using GPUs for the exam**, let me know, so I can see what I can do :).
:::

## Setup (Once)
So far, you have been using CPUs via [SDU](https://docs.cloud.sdu.dk/guide/resources-products.html#drawing-deic-interactive-hpc-sdu-k8s). However, our GPU resources are located on [AAU](https://docs.cloud.sdu.dk/guide/resources-products.html#drawing-deic-interactive-hpc-aau-k8s). You can distinguish by the logos beside the machine names:

```{figure} /figures/gpu_guide/logos.png
---
name: sdu-aau
width: 50%
---
```

The problem is that we **cannot** directly access our current folder `nlp` from SDU on AAU servers. This means that **we have to do setup again**. 

### What You Need to Do
1) Go to our workspace and try to start a Coder Python run, then select an **AAU CPU**: 
```{figure} /figures/gpu_guide/AAU-gpu.png
---
name: aau-gpu
width: 100%
---
```

2) Then, go to **[Class Setup](../book/class_setup.md)** and repeat the guide. That is, you need to create a new `nlp` folder in your AAU member files and mount the new `resources` AAU drive. 
> Consider adding a prefix to your job name `AAU_jobname` to more easily distinguish between SDU & AAU when pressing "run again".

3) Start the AAU CPU run and repeat the [virtual environment](../book/virtual_environments.md) setup. Install `pandas` as start. 

4) Close the CPU run when you are done !

:::{admonition} Upload Files to AAU
:class: tip, dropdown
In UCloud (or coder Python), you can drag files from your computer to AAU. So you can work on SDU and then move files to AAU. This is ideal as we don't have many CPU hours on AAU.
:::


## Which Machine to Pick? 
After having created your AAU setup, you are ready to open a AAU GPU:
```{figure} /figures/gpu_guide/gpu-overview.png
---
name: aau-gpu-overview
width: 100%
---
```

We currently have access to [Nvidia L4's](https://docs.cloud.sdu.dk/guide/resources-products.html#id2). As a rule of thumb, you will only need the `uc1-l4-1` (a single L4).

## Best Practice Principles for GPU
You can use GPUs if you need them, but keep these best practices in mind, so we use them wisely! 

### 1. GPUs for Running, CPUs for Development
**Only** use your AAU GPU for *running* the code. Writing and developing should be on **SDU** CPUs!

Of course, you can change the code / debug small things if you run something on GPU and end up realizing that it doesn't work... However, for bigger debugging sessions, switch to CPU! 

### 2. Keep Strict Time limits & Close your Run!
Try not to open a GPU run with more than a few hours on it at a time (you can always hit the "extend" button with `+1`):
```{figure} /figures/class_setup/step1-interface.png
---
name: interface
---
```

And **please close your run when you're done** (this is also important for CPU runs).

### 3. Make Sure You are Utilizing GPU Resources
Often you need to specify a parameter in your code to make it run on GPU (typically `cuda`).   

For instance, with a `transformers` model, you would specify: 
```python
from transformers import AutoModelForSequenceClassification
import torch

# set device: 
device = torch.device("cuda") if torch.cuda.is_available() else torch.device("cpu")

# load model and move to device
model = AutoModelForSequenceClassification.from_pretrained("distilbert/distilbert-base-cased").to(device) # move model to device (cpu or gpu)

```

You can check whether your GPU resources are utilized by writing `nvidia-smi` in the terminal of a GPU run:
```{figure} /figures/gpu_guide/smi_result.png
---
name: interface
---
Modified from [gpu-mart.com](https://www.gpu-mart.com/blog/monitor-gpu-utilization-with-nvidia-smi). The red underlines the memory usage and GPU-util (it is 0%, so the GPU is not used on the screenshot). If you had more than one GPU, there would be additional rows.
```