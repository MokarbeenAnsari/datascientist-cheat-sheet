# Jupyter Notebook & Conda Cheat Sheet

This cheat sheet covers some basic operations in Conda, a package and environment management system.

## Table of Contents
1. [How to see the version of Conda?](#how-to-see-the-version-of-conda)
2. [How to create a new Conda environment?](#how-to-create-a-new-conda-environment)
3. [How to list all Conda environments?](#how-to-list-all-conda-environments)
4. [How to activate a Conda environment?](#how-to-activate-a-conda-environment)
5. [How to add a Conda environment to Jupyter Notebook?](#how-to-add-a-conda-environment-to-jupyter-notebook)
6. [How to start Jupyter Notebook?](#how-to-start-jupyter-notebook)
7. [How to check if Jupyter Notebook is installed?](#how-to-check-if-jupyter-notebook-is-installed)
8. [How to install Jupyter Notebook?](#how-to-install-jupyter-notebook)

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

### How to add a Conda environment to Jupyter Notebook?

To use a specific Conda environment in Jupyter Notebook, you need to install Jupyter in that environment and add it as a kernel. Here's how you can do that:

1. Activate the Conda environment you want to add to Jupyter Notebook:

    ```bash
    conda activate myenv
    ```

2. Once the environment is activated, install `ipykernel`:

    ```bash
    conda install -c anaconda ipykernel
    ```

3. Add this environment to Jupyter:

    ```bash
    python -m ipykernel install --user --name=myenv
    ```

4. You can now start Jupyter Notebook. Once it's open, you can select the new kernel from the 'Kernel' menu.

### How to start Jupyter Notebook?

Starting a Jupyter Notebook is quite simple. Here's how you can do it:

1. Open a terminal or command prompt.

2. Navigate to the directory where you want to create or have your notebooks. You can do this using the `cd` command followed by the directory path. For example:

    ```bash
    cd /path/to/your/directory
    ```

3. Once you are in the desired directory, start Jupyter Notebook by typing the following command and pressing Enter:

    ```bash
    jupyter notebook
    ```

This will start the Jupyter Notebook server and open your web browser. The Jupyter Notebook homepage will show a list of notebooks, files, and subdirectories in the directory where the notebook server was started.

### How to check if Jupyter Notebook is installed?

To check whether Jupyter Notebook is installed or not, you can use the following command in the terminal:

    jupyter --version

If Jupyter is installed, this command will display the version of Jupyter that's installed on your system. If it's not installed, the system will not recognize the command and may output a message such as "command not found" or " 'jupyter' is not recognized as an internal or external command, operable program or batch file."

### How to install Jupyter Notebook?

You can install Jupyter Notebook using Conda or pip. Here's how you can do it:

Using Conda:

If you have Anaconda or Miniconda installed, you can install Jupyter Notebook using the `conda` command. Open a terminal or command prompt and type:

    conda install -c anaconda jupyter

This command installs Jupyter Notebook from the Anaconda distribution channel.

Using pip:

If you have Python installed and prefer to use pip, you can install Jupyter Notebook by opening a terminal or command prompt and typing:

    pip install notebook

Remember that you need to have Python installed on your machine to use pip. If you have both Python 2 and Python 3 installed, you might need to use `pip3` instead of `pip`.

After installing, you can launch Jupyter Notebook by typing:

    jupyter notebook

This command starts the Jupyter Notebook server and should automatically open the server's dashboard in your default web browser.
