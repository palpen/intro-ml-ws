# Build a Loan Default Machine Learning Model using Python

#### Instructors

* Hudson Pimenta ([@hudsonps15](https://twitter.com/hudsonps15))
* Palermo Penano ([@pspenano](https://twitter.com/pspenano))

This repository contains materials for a 3-part machine learning workshop taught at Scotiabank. We will cover key parts of a standard data science development lifecycle and build a loan default predictor model using Python. 

The topics covered in each session are as follows (click the topics below to view the notebook covered in that session):

- April 8, 2021

- - Setting up your development environment (see below)
  - [Analyzing your dataset](https://github.com/palpen/intro-ml-ws/blob/main/exploration.ipynb)

- April 15, 2021

- - [Feature engineering](https://github.com/palpen/intro-ml-ws/blob/main/feature_eng.ipynb)
  - [Validation and test set](https://github.com/palpen/intro-ml-ws/blob/main/feature_eng.ipynb)
  - [Train a decision tree classifier](https://github.com/palpen/intro-ml-ws/blob/main/model_pt1.ipynb)

- April 22, 2021

- - [Train a decision tree classifier (continued)](https://github.com/palpen/intro-ml-ws/blob/main/model_pt1.ipynb)
  - [Train a random forest classifier](https://github.com/palpen/intro-ml-ws/blob/main/model_pt2.ipynb)
  - Interpreting your model (TBD)

# Lending Club Dataset

We will use a dataset containing real world loan applications from the [Lending Club](https://www.lendingclub.com/). The dataset contains information on loan amounts, interest rates, customer demographic data, etc.

You can download it from Kaggle on [this page](https://www.kaggle.com/wordsforthewise/lending-club). Note that you'll need a Kaggle account to download the file.

The dataaset we will use is named `accepted_2007_to_2018Q4.csv.gz`. You can ignore the other file. Download the file, move it to the `data` folder of the cloned version of this repository and extract its content. You should see a single csv file at the end.

# Installing `conda` 

The steps below installs [conda](https://conda.io/projects/conda/en/latest/index.html#)---a popular package and environment manager for Python used widely in data science, machine learning, and scientific programming. `conda` allows you to customize your development environment for your project. This avoids cluttering your computer with packages that you may not need for all projects which may cause library dependencies that conflict with one another.

More importantly, `conda`  enables other people to recreate the environment you used to run your code. It ensures that the libraries and their version that they will use to run your code will be identical to the one you used when you developed it.

Note: Miniconda only installs Python and the `conda` package manager. Anaconda installs Python, `conda` and a number of commonly used libraries for data science (pandas, numpy, matplotlib, scikit-learn, etc). It is a much larger file.

### Windows

1. Go to https://docs.conda.io/en/latest/miniconda.html and download the Python 3.8 Miniconda3 Windows 64-bit file (the 64-bit version should work for most modern Windows operating system)

2. Open the `.exe` file and and follow the setup instructions. Say yes to all the default configuration without changing any of the recommended settings

3. Once installed, you can open a command line prompt by going to your search bar and typing "Anaconda Powershell Prompt". You should see a window open that looks like this

   <img src="./imgs/anaconda_prompt.png" alt="anaconda_prompt" style="zoom:15%;" />

4. Test your installation by running the command `conda list` in the prompt. You should see a list of installed packages appear if the installation was succesful.

### MacOS

1. Go to https://docs.conda.io/en/latest/miniconda.html and download the Python 3.8 Miniconda3 MacOSX 64-bit pkg file
2. Once downloaded, click the `.pkg` file and follow the prompts on the installer screen. Accept the default settings for now
3. Hit `Command + Space` on your keyboard to open Spotlight Search to search for applications. Search for **Terminal**
4. In the terminal, run the command `conda list`. You should see a list of installed packages appear if the installation was succesful.

# Virtual Environments

## Creating a virtual environment

The instructions below shows you how to create a virtual environment using `conda` and subsequently starting a `Jupyter Notebook`. The steps are for the Windows OS, but is very similar to Mac OS, the commands for which I have added in parenthesis.

1. Download this repository as a zipped file from GitHub (or clone the repository if you have Git installed and are familiar with commands for `git`)

   <img src="./imgs/repo_zip.png" alt="repo_zip" style="zoom:20%;" />

2. Extract all its contents to a directory on your computer. Note the path to the folder where the GitHub repository was extracted. You can get the folder location by right clicking on it and going to Properties

3. Open the Anaconda Powershell Prompt by searching for it in your Windows search bar (*MacOS*: In your Applications folder, look and open the **Terminal** app).

4. Change the current directory to the folder that you downloaded and extracted in steps 1 and 2 using the `cd` command (which stands for `current directory`)

   __Tip:__ You can get the full path to any folder/file by right clicking the folder/file while holding down the _Shift_ key and choosing "Copy as path"

   <img src="./imgs/anaconda_cd_proj_folder.png" alt="anaconda_cd_proj_folder" style="zoom:50%;" />

   If you succesfully changed the working directory in the Anaconda Powershell Prompt to the project directory, you should be able to list all the files in the folder using the `dir` command (*MacOS*: use `ls` instead )

   ​																<img src="./imgs/dir_folder.png" alt="dir_folder" style="zoom:40%;" />

5. To build your development environment and install all the libraries required, run the command `conda env create` in the Anaconda PowerShell Prompt (*MacOS*: Terminal) inside of the GitHub project folder

   <img src="./imgs/run_conda_env_create.png" alt="run_conda_env_create" style="zoom:20%;" />

   If succesful, you should have a conda environment named `intro-ml-ws` that will have all the the packages you need to follow this workshop and execute the codes in the notebook.

   You can list all the available conda environments by running the command `conda env list`

## Activating your virtual environment

1. Activate the environment with  `conda activate intro-ml-ws`.

2. Start a notebook server by executing `jupyter notebook`

   <img src="./imgs/start_notebook.png" alt="start_notebook" style="zoom:50%;" />

   The server will be located in http://localhost:8888. Open this url in your favourite browser and click on any one of the files ending with `.ipynb`  to open a notebook.



