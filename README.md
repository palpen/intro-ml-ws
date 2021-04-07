# Build a Loan Default Machine Learning Model using Python

#### Instructors

* Hudson Pimenta ([@hudsonps15](https://twitter.com/hudsonps15))
* Palermo Penano ([@pspenano](https://twitter.com/pspenano))

This repository contains materials for a 3-part machine learning workshop named taught at Scotiabank.

The data used in the workshop is a csv file of accepted loan applications named `accepted_2007_to_2018Q4.csv.gz` from Kaggle. The dataset can be downloaded from the url below:

https://www.kaggle.com/wordsforthewise/lending-club

The workshop is split into 3 sessions that will cover the key parts of a standard data science / machine learning development lifecycle. These broadly include

* Setting up your development environment
* Analyzing your dataset
* Feature engineering
* Training, validating, and evaluating models
* Model interpretation

# Setting up your development environment using the `conda`  package manager

The steps below installs [conda](https://conda.io/projects/conda/en/latest/index.html#)---a popular package and environment manager for Python used widely in data science, machine learning, and scientific programming. `conda` allows you to customize your development environment based only on the libraries you need for a given project. This avoids cluttering your computer with packages you don't need and potentially causing issues with conflicting dependencies among packages you have installed. 

Using a package manager such as `conda` also enables other people to recreate the environment you ran your code in thereby alloweing them to run your code on their own computer. The instructions below will install Miniconda and show you how to create your own environment.

Note: Miniconda only installs Python and the `conda` package manager. Anaconda installs Python, `conda` and a number of commonly used libraries for data science (pandas, numpy, matplotlib, scikit-learn, etc). It is a much larger file.

### Windows

1. Go to https://docs.conda.io/en/latest/miniconda.html and download the Python 3.8 Miniconda3 Windows 64-bit file (the 64-bit version should work for most modern Windows operating system)

2. Open the `.exe` file and and follow the setup instructions. Say yes to all the default configuration without changing any of the recommended settings

3. Once installed, you can open a command line prompt by going to your search bar and typing "Anaconda PowerShell Prompt". You should see a window open that looks like this

   <img src="./imgs/anaconda_prompt.png" alt="anaconda_prompt" style="zoom:15%;" />

4. Test your installation by running the command `conda list` in the prompt. You should see a list of installed packages appear if the installation was succesful.

### MacOS

1. Go to https://docs.conda.io/en/latest/miniconda.html and download the Python 3.8 Miniconda3 MacOSX 64-bit pkg file
2. Once downloaded, click the `.pkg` file and follow the prompts on the installer screen. Accept the default settings for now
3. Hit `Command + Space` on your keyboard to open Spotlight Search to search for applications. Search for **Terminal**
4. In the terminal, run the command `conda list`. You should see a list of installed packages appear if the installation was succesful.

### Creating a virtual environment

The instructions below shows you how to create a virtual environment using `conda` and subsequently starting a `Jupyter Notebook`. The steps are for the Windows OS, but is very similar to Mac OS, the commands for which I have added in parenthesis.

1. Download this repository as a zipped file from GitHub (or clone the repository if you have Git installed and are familiar with commands for `git`)

   <img src="./imgs/repo_zip.png" alt="repo_zip" style="zoom:20%;" />

2. Extract all its contents to a directory on your computer. Note the path to the folder where the GitHub repository was extracted. You can get the folder location by right clicking on it and going to Properties

3. Open the Anaconda Prompt by searching for it in your Windows search bar (*MacOS*: In your Applications folder, look and open the **Terminal** app).

4. Change the current directory to the folder that you downloaded and extracted in steps 1 and 2 using the `cd` command (which stands for `current directory`)

      <img src="./imgs/anaconda_cd_proj_folder.png" alt="anaconda_cd_proj_folder" style="zoom:50%;" />

   If you succesfully changed the working directory in the Anaconda Prompt to the project directory, you 		should be able to list all the files in the folder using the `dir` command (*MacOS*: use `ls` instead )

   ​	<img src="./imgs/dir_folder.png" alt="dir_folder" style="zoom:40%;" />

5. To build your development environment and install all the libraries required, run the command `conda env create` in the Anaconda Prompt (*MacOS*: Terminal) inside of the GitHub project folder

   <img src="./imgs/run_conda_env_create.png" alt="run_conda_env_create" style="zoom:20%;" />

   If succesful, you should have a conda environment named `intro-ml-ws` that will have all the the packages you need to follow this workshop and execute the codes in the notebook.

   You can list all the available conda environments by running the command `conda env list`

6. Activate the environment by executing `conda activate intro-ml-ws`.

7. Start a notebook server by executing `jupyter notebook`

   <img src="./imgs/start_notebook.png" alt="start_notebook" style="zoom:50%;" />

   The server will be located in http://localhost:8888. Open this url in your favourite browser and click on any one of the files ending with `.ipynb`  to open a notebook.



