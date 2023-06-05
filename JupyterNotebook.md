# Jupyter Notebook & Conda Cheat Sheet

This cheat sheet covers some basic operations in Conda, a package and environment management system.

## Table of Contents
1. [How to see the version of Conda?](#how-to-see-the-version-of-conda)
2. [How to create a new Conda environment?](#how-to-create-a-new-conda-environment)
3. [How to list all Conda environments?](#how-to-list-all-conda-environments)
4. [How to activate a Conda environment?](#how-to-activate-a-conda-environment)

### How to see the version of Conda?

To see the version of Conda you have installed, open a terminal or command prompt and type the following command:

    conda --version

### How to create a new Conda environment?

To create a new Conda environment, use the `conda create` command followed by the `-n` flag (for name) and the name of the environment. You can also specify the Python version. Here's an example:

    conda create -n myenv python=3.7

This will create a new environment named `myenv` with Python 3.7.

### How to list all Conda environments?

To list all your Conda environments, use the following command:

    conda env list

This will display a list of all Conda environments on your system.

### How to activate a Conda environment?

To activate a Conda environment, use the `conda activate` command followed by the name of the environment. Here's an example:

    conda activate myenv

This will activate the environment named `myenv`.
