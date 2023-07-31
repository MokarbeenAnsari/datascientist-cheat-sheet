# Jupyter Notebook & Conda Cheat Sheet

This cheat sheet covers some basic operations in Conda, a package and environment management system.

## Table of Contents
1. [How to see the version of Conda?](#how-to-see-the-version-of-conda)
2. [How to create a new Conda environment?](#how-to-create-a-new-conda-environment)
3. [How to list all Conda environments?](#how-to-list-all-conda-environments)
4. [How to activate a Conda environment?](#how-to-activate-a-conda-environment)
5. [How to add a Conda environment to Jupyter Notebook?](#how-to-add-a-conda-environment-to-jupyter-notebook)
6. [How to see the list of Conda environments added in Jupyter Notebook?](#how-to-see-the-list-of-conda-environments-added-in-jupyter-notebook)
7. [How to remove a Conda environment from Jupyter Notebook?](#how-to-remove-a-conda-environment-from-jupyter-notebook)
8. [How to start Jupyter Notebook?](#how-to-start-jupyter-notebook)
9. [How to check if Jupyter Notebook is installed?](#how-to-check-if-jupyter-notebook-is-installed)
10. [How to install Jupyter Notebook?](#how-to-install-jupyter-notebook)
11. [How to remove Conda environment?](#how-to-remove-conda-environment)
12. [How to clone Conda environment?](#how-to-clone-conda-environment)

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

### How to see the list of Conda environments added in Jupyter Notebook?

To see the list of Conda environments added to Jupyter Notebook as kernels, you can use the `jupyter kernelspec list` command in the terminal. Here's the command:

   ```bash
   jupyter kernelspec list
   ```

This command lists all available Jupyter kernels.

### How to remove a Conda environment from Jupyter Notebook?

To remove a Conda environment that you've added to Jupyter Notebook, you'll need to uninstall the corresponding kernel. You can do this using the `jupyter kernelspec uninstall` command followed by the name of the environment. Here's an example:

```bash
jupyter kernelspec uninstall myenv
```
This command will uninstall the `myenv` kernel. After running this command, you'll no longer be able to use the `myenv` environment in Jupyter Notebook, but the Conda environment itself will still exist unless you remove it using the Conda remove commands provided in the earlier section.

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

### How to remove Conda environment?

To delete a Conda environment, use the `conda remove` command followed by the `--name` flag and the name of the environment you want to remove. Here's an example:

    conda remove --name myenv --all
    
This command will remove the environment named myenv and all its packages.

Alternatively, you can use the conda env remove command followed by the --name flag and the name of the environment. Here's an example:

    conda env remove --name myenv
    
This command will also remove the environment named myenv, including its packages.
