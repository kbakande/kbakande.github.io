---
layout: post
title: Poetry Managed Jupyter Notebooks
---

Jupyter is a tool used to run notebooks, which are interactive documents where you can write and execute code. Jupyter requires a kernel to execute code in the notebook. A kernel is a computational engine that runs the code contained in the notebook, and it has access to the Python packages that are installed in its environment.

Poetry is a dependency manager that creates and manages virtual environments for Python projects. These virtual environments are isolated, meaning that any packages installed within them are separate from the system Python installation, ensuring that dependencies for different projects do not conflict.

To run a Jupyter notebook using a Poetry virtual environment, the virtual environment needs to be made available as a kernel within Jupyter. This is achieved by installing the ipykernel package inside the Poetry environment. ipykernel allows Jupyter to use the Poetry-managed virtual environment as a kernel.

Once ipykernel is installed, the Poetry environment can be registered as a kernel for Jupyter. When you run poetry run jupyter notebook, it starts Jupyter using the Poetry virtual environment, and you'll be able to select this environment as a kernel for your notebooks. As a result, any dependencies you've installed via Poetry will be available within the notebook, allowing you to run your code with the correct set of packages.

To ensure that a Jupyter notebook you're running uses the Poetry virtual environment, you need to set up Jupyter to use the Python interpreter from the Poetry-managed virtual environment. Here's how you can do that:

Steps to Use Poetry Virtual Environment with Jupyter Notebook:
1. Install ipykernel
First, make sure that the ipykernel package is installed in your Poetry-managed virtual environment. This package allows Jupyter to use the virtual environment as a kernel.

Activate your Poetry environment:

```bash
poetry shell
```

Then, install ipykernel:

```bash
poetry add ipykernel
```

2. Add Poetry Virtual Environment to Jupyter as a Kernel
After installing ipykernel, you need to add the Poetry environment as a kernel to Jupyter.

Run this command:

```bash
python -m ipykernel install --user --name=my-poetry-env --display-name "Poetry Environment"
```
* Replace my-poetry-env with a name you'd like to give to this virtual environment kernel.
* "Poetry Environment" is the name that will appear in Jupyter when selecting the kernel for the notebook.

3. Open Jupyter Notebook
Now, start Jupyter Notebook (if you don't have it installed yet, you can add it via Poetry with poetry add notebook).

Run:

```bash
poetry run jupyter notebook
```

This will start the Jupyter notebook, and you'll be able to open a notebook from the browser.

4. Select the Poetry Environment Kernel
Once Jupyter is running, open your notebook. To switch the kernel to the Poetry environment:

In the Jupyter notebook interface, click on Kernel > Change kernel.
Choose the Poetry Environment (or the name you gave to the kernel).
Now, your notebook will be using the Poetry-managed virtual environment, with all the dependencies you installed through Poetry available within the notebook!