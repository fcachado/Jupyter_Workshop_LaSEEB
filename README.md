# Installation

1. To set the virtual environment to run this tutorial we will use conda. If you do not have, I recommend the [Miniconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/)

2. In Windows, during the installation process to avoid conflicts with possible whitespaces in the path, install in the folder:

    ```bash
    C:\miniconda3
    ```

3. Download the .zip file and extract the folder inside to your Documents folder. Rename the folder to:

    ```bash
    Jupyter_Workshop_LaSEEB
    ```

4. Then create the 2 environments - JW_LaSEEB_1 and JW_LaSEEB_2. All the required packages will be automatically installed.
   - In Windows using the shortcut created in the startup menu "Anaconda Prompt" (replace <current_user> by your user name):

      ```bash
      cd C:\Users\<current_user>\Documents\Jupyter_Workshop_LaSEEB
      conda env create -f environment_1.yml
      conda env create -f environment_2.yml
      ```

   - In Linux/MacOS using the terminal:

      ```bash
      cd ~/Documents/Jupyter_Workshop_LaSEEB
      conda env create -f environment_1.yml
      conda env create -f environment_2.yml
      ```

5. Activate environment, can not activate both at the same time:

   - JW_LaSEEB_1, to run all script started by "JW_LaSEEB_1_":

      ```bash
      conda activate JW_LaSEEB_1
      conda install -c conda-forge nodejs
      npm install -g configurable-http-proxy
      ```

   - JW_LaSEEB_2, to run all script started by "JW_LaSEEB_2_":

      ```bash
      conda activate JW_LaSEEB_2
      conda install -c conda-forge nodejs
      npm install -g configurable-http-proxy
      jupyter labextension install @jupyter-widgets/jupyterlab-manager jupyter-matplotlib jupyterlab-datawidgets itkwidgets
      ```

6. To open JupyterLab:

    ```bash
      jupyter lab
    ```

7. Deactivate the current environment, to change to the other one or to remove:

    ```bash
      conda deactivate
    ```

8. If you want to delete the virtual environment, first it needs to be deactivated:

    ```bash
      conda env remove --name <name-of-environment>
    ```
