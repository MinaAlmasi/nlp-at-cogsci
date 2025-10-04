# Virtual Environments 
When we have been running a job on UCloud's *Coder Python*, we have been reinstalling packages for each new run. We can avoid this by using *virtual environments*, which appear as a folder (typically named `.venv`).

The `venv` folder contains a seperate Python installation along with any packages you install inside it. In practice, this allows you to have multiple Python versions and package sets on your system without any conflicts:

![illustration of three virtual environments](/figures/advanced_workflow/python-virtual-envs.jpg)


In addition to improving your UCloud flow, virtual environments are usually created for each coding project. This gives us better control over the packages and their versions (our code's *dependencies*), ensuring the code is **reproducible**.

## Using environments with `venv` 
While there are several ways to use and install virtual environments, this course will using Python's built-in module `venv`! Proceed to the next pages for a tutorial!