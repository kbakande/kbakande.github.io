---
layout: post
title: Jupyter Notebook  Poetry-managed virtual environment libraries
---

1. CD into an exiting poetry managed project and add jupyter as dev dependency.

```bash
 cd my_existing_project
 poetry add jupyter --group dev
```

2. Create/start a Poetry virtual environment

    ```bash
        poetry shell
    ```
3. 

    ```bash
        poetry add ipykernel --group dev
    ```
4. Create a new kernel linked to the virtual environment

```python
python -m ipykernel install --user --name=my_project_kernel
```
5. Launch Jupyter Notebook
  ```bash
  jupyter notebook
  ```
6. Select the Correct Kernel in Jupyter

 * Once Jupyter Notebook is opened in your browser, 
 * create a new notebook or open an existing one. 
 * Then, change the kernel to the one you just created (my_project_kernel or whatever name you chose) by clicking on Kernel > Change kernel > my_project_kernel
