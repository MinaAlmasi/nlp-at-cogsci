<style>

.footnote-list {
    display: none;
}
</style>

# UCloud. Best Practice
UCloud is an AWESOME resource for running state-of-the-art NLP tools such as LLMs. It's almost like a superpower, which brings me to this: 

```{figure} /figures/ucloud_best_practice/spidey.png
---
height: 400px
name: spider-man-saying-with-great-power-comes-great
---
"With great power comes great responsibility"!! 
```


## No, but why?
The reason that I keep pestering about UCloud is that we're running **on shared resources**. This means: 
1. We have a limited set of hours/credits for CPU and GPU that we share as a class (the same goes for storage...)
2. Other people (in other courses) might be waiting in line for the machine you are currently using! 

**This does not mean that you should be afraid to use our resources!** It means that you should try to use them *well*.

## General Guidelines for Responsible Use
Make sure you read the guidelines below carefully. As with any guidelines, there might exceptions (ask me if in doubt!)

:::{dropdown} 1. Always close your job if you don't need it !
Especially important for GPUs!
:::
:::{dropdown} 2. Keep strict time limits for jobs
Try *not* to open a job with more than a few hours on it at a time (you can always hit the "extend" button with `+1`):
```{figure} /figures/ucloud_best_practice/extend-job.png
---
name: interface
---
```
This makes it less critical if you forget to close a job (always try to do so!). It is **especially important for GPU runs** where we have more limited resources.
:::

:::{dropdown} 3. Use the smallest machine possible for any kind of task 
This does not mean you should never use a big CPU (`v16CPUs` or `v32CPUs`) or that you should be afraid to use GPUs. However, you will rarely need `v16CPUs`. Simple classification often only needs `2vCPUs`or `4vCPUs`. 

Feel free to experiment & start jobs with various machine sizes. **Just make sure to down-size if you see that you aren't using the right one (see point 6)**

:::{dropdown} For class, I'll recommend!
:color: warning
Prior to each class, I tell you which machine size I recommend for today's exercises!
:::
:::

:::{dropdown} 4. GPUs are mostly for running big models, CPUs are for everything else.
GPUs will mostly be relevant for running big models (LLMs mostly). You'll get a feel for when to use what in class, but you can also ask me.
:::

:::{dropdown} 5. Use CPU for code development, run ready code on GPU
Even if you plan on using LLMs, **only** use your GPU for *running* the code. Writing and developing should be on CPUs! 
- That means doing dummy runs with smaller LLMs (or deactivating the LLM in your pipeline)
- Come talk to me if you need help with this!

**Of course, you can change the code / debug small things if you run something on GPU and end up realizing that it doesn't work...** However, for bigger debugging sessions, switch to CPU! 
:::


:::{dropdown} 6. Ensure that you are *fully* utilizing the chosen machine (if not: downsize)
Generally, you can check the usage on your job before you "open interface". This is an example of an under-utilized machine:
```{figure} /figures/ucloud_best_practice/ucloud-usage.png
---
name: ucloud-usage
---
```

Look at the machine when it's actually being used! If your code is not too slow & you see a pattern like this, you know the machine size is right for you:
```{figure} /figures/ucloud_best_practice/ucloud-usage-high.png
---
name: ucloud-usage-high
---
```

NB. If you see high activity like this, and the code is taking hours, it may be worth up-sizing. You can always down-size again!

:::{dropdown} Special cases for GPU (remember to optimize!)
:color: warning
With GPU, you often you need to **specify a parameter in your code** to make it run on GPU (typically `cuda`).   

For instance, with a `transformers` model, you would specify: 
```python
from transformers import AutoModelForSequenceClassification
import torch

# set device: 
device = torch.device("cuda") if torch.cuda.is_available() else torch.device("cpu")

# load model and move to device
model = AutoModelForSequenceClassification.from_pretrained("distilbert/distilbert-base-cased").to(device) # move model to device (cpu or gpu)

```

 write `nvidia-smi` in the terminal of a GPU run:
```{figure} /figures/gpu_guide/smi_result.png
---
name: interface
---
Modified from [gpu-mart.com](https://www.gpu-mart.com/blog/monitor-gpu-utilization-with-nvidia-smi). The red underlines the memory usage and GPU-util (it is 0%, so the GPU is not used on the screenshot). If you had more than one GPU, there would be additional rows.
```
:::
:::

:::{dropdown} 7. Clear out storage you are not using!
NLP tends to fill up a ton, turns out LLMs are *really* that big! If you end up downloading data or models that you don't need (e.g., for the exam), make sure to delete them.

:::{dropdown} NB. STORAGE WILL BE DELETED MARCH 1ST
:color: warning
To clear up space for the next cogsci courses, your files will be deleted after the course has ended. 
* If you need to keep something for your msc thesis or other personal use, make sure to transfer to your own computer!
:::

:::

:::{admonition} You can always ask me :)
:class: important
Again, whether it is an exception or just a question, please always feel free to ask me when in doubt! I can help you choose machines or clear up any confusion.
:::

## Is UCloud Slow Today?
If you are following the guidelines and find UCloud slow, it might not be your fault. Sometimes, UCloud might be down:
```{tip} 
You can check whether UCloud is down at: [https://status.cloud.sdu.dk](https://status.cloud.sdu.dk/)
```