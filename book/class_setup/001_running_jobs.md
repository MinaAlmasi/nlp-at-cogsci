# Step 1. Run a "Job" on UCloud

The sections below gives you a step-by-step on how to get started with UCloud. A short summary of this is:
1. Find `Coder Python` on the workspace `E26_LICS_NaturalLanguageProcessing`
2. Mount folders `nlp` (created within your own member files) and `resources` (shared drive provided by me)
3. Choose an appropriate machine size for X amount of hours 
4. Submit a job !

## Choose the Right Workspace
Go to [https://cloud.sdu.dk/app](https://cloud.sdu.dk/app). In the top right corner, choose the workspace `E26_LICS_NaturalLanguageProcessing`:

```{figure} ../figures/class_setup/step1-choose-workspace-2026.png
---
height: 130px
name: choose-right-workspace
---

:::{tip} 
Hit the *star button* to favourite the workspace :)
:::

```
> If you are not part of the workspace yet, check instructions on [Brightspace](https://brightspace.au.dk/d2l/home/216059) or ask me.

### Find Coder Python
On the left sidebar, find **Applications** by clicking the **shopping cart**:

```{figure} ../figures/class_setup/step1-shopping-cart.png
---
height: 200px
name: shopping_cart
---
````

Find `Coder`:

```{figure} ../figures/class_setup/step1-coder-python.png
---
name: coder-python
---
```

#### Choose Version
1. Select `Python` not `Base` 
2. keep the version at `1.131.0` for consistent bug-fixing.
```{figure} ../figures/class_setup/step1-select-python-and-version-2026.png
---
name: coder-python-select-version
---
```

```{tip} 
Hit the *star button* to favourite Coder Python *after* selecting the correct version. Then you will more easily be able to find it next time!
```

### Defining Your Job 
Start by giving your job a name (1).

:::{admonition} Give jobs meaningful names!
:class: warning, dropdown
**Try to give your job a meaningful name and avoid using the same name for several jobs.**

UCloud saves relevant files under each job name upon ending them. If you end a job prematurely and need a specific version of the files for another job, you can look in the "ended" job! Easier when you can distinguish between jobs :D
:::

Select the amount of hours (2) and select "CPU" as machine type (3)
```{figure} ../figures/class_setup/step1-define-job-2026.png
---
name: define job
---
```

#### Selecting the right machine (CPU)
For now, go ahead an select the smallest CPU machine `1vCPU` (longer name: `cpu-amd-zen5-1-vcpu`). You won't need more for setting up! 

```{figure} ../figures/class_setup/step1-vcpus.png
---
name: select right cpu
---
```

:::{admonition} Selecting a Machine: Be Mindful!
:class: warning
The machine size (i.e., amount of ram) depends on the NLP task, with later classes needing bigger machines (and even GPUs!). Please read the sections [UCloud: Best Practice](/book/ucloud_best_practice.md) for how to be mindful about our shared resources! We don't have unlimited!

**I will also recommend a machine size prior to each class, where you'll begin to get a feel for it.**
:::

(mounting-folders)=
#### Mounting Folders 
Scroll down to **Select folders to use** and click on **Add folder**:
```{figure} ../figures/class_setup/step1-add-folder-2026.png
---
name: add folder
---
```
> Only the folders you choose here will be available for the duration of this UCloud job.

Now press on empty white bar (which says *No directory selected*):
```{figure} ../figures/class_setup/step1-add-folder-part-2-2026.png
---
name: add folder
---
```

##### Add the `nlp` Folder

:::{warning}
Now it becomes important that we are all **streamlined** !
:::


THE FIRST TIME: 
1. Ensure you are in your **Member files** (i.e., folder with your name)
2. Press **Create folder**
3. Call the folder `nlp` (lowercase!!!):
```{figure} ../figures/class_setup/step1-create-folder.png
---
name: create folder
---
```
When you have created the folder (or if you had already), press **use** to mount the `nlp` folder:
```{figure} ../figures/class_setup/step1-nlp.png
---
name: use nlp
---
```

##### Add the `resources` Folder (Class Resources)
The class **resources** is a shared folder (created by me) which contains necessary data and models that you might need for an exercise. 

**Press to add another folder**:

```{figure} ../figures/class_setup/step1-add-another-folder.png
---
name: add another folder
---
```

:::{admonition} Always mount it, even if you don't need it!
:class: tip, dropdown
We may not always need this folder (or it may only be needed optionally).

**However, I recommend always mounting it to make your life easier!** This way, you won't need to end a job and make a new one, if you realize mid-way that you wanted the **resources** folder.
:::


**Press the small arrow** (1), choose the drive **resources** (2) and **press use folder** (3):
```{figure} ../figures/class_setup/step1-resources-2026.png
---
name: resources folder
---
```

### Template Setup
**If your setup looks something like the one below, you are ready to press the green Submit button** above the estimated costs:
```{figure} ../figures/class_setup/step1-template.png
---
name: template setup
---
```

## Open the Interface
After pressing Submit, you will get a loading screen before seeing **JOB_NAME is now running**. You can now press **Open Interface:**


```{figure} ../figures/class_setup/step1-interface.png
---
name: interface
---
```


:::{admonition} Extending the job
:class: tip
You can easily extend your job by an hour (+1) or more with the three buttons below **Time Remaining** on the left box.

See [UCloud: Best Practice](/book/ucloud_best_practice.md).
:::

### Detail: "Trusting the workspace" 
Newer versions of Coder Python on UCloud show this banner when opening the interface. Press **Manage**
```{figure} ../figures/class_setup/step1-restricted-mode-banner.png
---
name: restricted mode (banner)
---
```

Press **Trust** to open up for the full functionality of Coder Python:
```{figure} ../figures/class_setup/step1-restricted-mode-modal.png
---
name: restricted mode (modal)
---
```
