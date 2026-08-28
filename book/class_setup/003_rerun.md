# Step 3. Re-run, don't start over at Step 1!
After doing [Step 1](/book/class_setup/001_running_jobs.md) and [Step 2](/book/class_setup/002_jupyter.md), you hopefully closed your UCloud run! **The good news is that everything will be easier next time.** A short summary of this guide: 
1. Find the jobs page
2. Find a previous job and press "re-run" 
3. Update that previous job with new details (e.g., new name and/or different machine size)
4. Run your new job, created from a previous one. 

:::{admonition} You don't actually need to open a new job
:class: warning
If you completed  [Step 1](/book/class_setup/001_running_jobs.md) and [Step 2](/book/class_setup/002_jupyter.md), great job! (no pun intended). 

You don't need to actually open a new run with this guide, I suggest you just read through the guide for now (it'll serve you well!).
:::

## Find the Jobs page
On the left sidebar, the last symbol in the top is for "jobs". Click on this.
```{figure} ../figures/class_setup/step3-jobs-sidebar.png
---
name: jobs-sidebar
---
```
:::{admonition} Your active jobs are also here
:class: tip, dropdown
This page also shows if you have any active jobs. This will be useful later, when some of you might want to run code in the background (e.g., overnight). I will introduce this to you in class (see [Tmux](/book/tmux.md)).
:::


## Re-running
Press on any previous job (1) and press **Run Again** (2):

```{figure} ../figures/class_setup/step3-rerunning.png
---
name: re-run
---
```

### Re-configure your job
You will meet the same job settings as you had for the previous one:

```{figure} ../figures/class_setup/step3-run-prev-job.png
---
name: re-run-prev-job
---
```

Go ahead and update settings (e.g., new job name, diff. machine size ...):
```{figure} ../figures/class_setup/step3-new-job.png
---
name: new job!
---
```

### Submit & Code again!
When you have updated your job, press Submit to get coding again!
```{figure} ../figures/class_setup/step3-submit-button.png
---
name: new job!
---
```