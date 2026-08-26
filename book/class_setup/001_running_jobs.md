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

This can be important as UCloud saves relevant files under each job name upon ending them. Did you end a job prematurely in one class and need a specific version of the files in another? Look at the job!
:::

Select the amount of hours (2) and the machine type (3):
```{figure} ../figures/class_setup/step1-define-job.png
---
name: define job
---
```
> For now, select the smallest machine! You don't need more for setting up!

:::{admonition} Selecting a Machine: Be Mindful!
:class: warning
Selecting the machine type depends on how much memory and power you need. This will vary throughout the course! But we need to be mindful, since we do not have unlimited credits. Please read the sections on [UCloud:Best Practice](/book/ucloud_best_practice.md)
:::

(mounting-folders)=
#### Mounting Folders 
Go down to "select folders to use" and click on "add folder". The folders you choose here will be the ones available to you during the run:
```{figure} ../figures/class_setup/step1-add-folder.png
---
name: add folder
---
```
#### Add the `nlp` Folder
Here it becomes important that we are all **streamlined**. 

If it is your first time: ensure you are in your `member files` folder (1), then press `create folder` (2). **Call the folder `nlp`**:
```{figure} ../figures/class_setup/step1-create-folder.png
---
name: create folder
---
```
Press `use` to mount the `nlp folder`:
```{figure} ../figures/class_setup/step1-nlp.png
---
name: use nlp
---
```

#### Adding the `resources` Folder (Class Resources)
Now, add another folder:
```{figure} ../figures/class_setup/step1-add-another-folder.png
---
name: add another folder
---
```
> Note: We may not always need this folder (or it may only be needed optionally), but I suggest always mounting it to make your life easier! It will contain necessary data and models you might want to load.

Here, we want to press the little arrow (1), choose the shared drive `resources` (2) and press `use folder`:
```{figure} ../figures/class_setup/step1-resources.png
---
name: resources folder
---
```

### Template Setup
If your setup looks something like this, you are ready to press the green `submit` button above the estimated costs:
```{figure} ../figures/class_setup/step1-standard.png
---
name: standard setup
---
```

## Open the Interface
When having pressed `submit`, you will be met with a loading screen before seeing `job_name is now running`. Go ahead and press the "open interface" !


```{figure} ../figures/class_setup/step1-interface.png
---
name: interface
---
```

> Note: You can easily extend your job by an hour (+1) or more with the buttons underneath the timer! 