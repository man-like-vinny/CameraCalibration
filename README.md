# CS410 Assignment 1

## Introduction

In this assignment, you will have be working on the provided `ipynb` notebook, 
where you will fill in necessary pieces of code to complete the stereo pipeline. 
Follow the instructions below to get started. Note that we a [Troubleshooting](#troubleshooting) section has been added at the bottom of the page where add any common problems (& solutions) will be added as they arise.

## Setup
1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html). Choose your OS, Architecture and version of Python. The notebook has been tested with Python 3.8, however 3.9 should be ok too. Let us know if you have any problems. _Skip this step if you have anaconda or miniconda already installed with Python 3.5+_
1. Create a conda environment, using the following command. On Windows, open the installed **Conda Prompt** (or **Anaconda Prompt**) to run this command. On MacOS and Linux, you can just use a **terminal** window to run the command.: `conda create -n cs410_hw1 --yes`. Confirm the packages marked for installation if prompted.
1. This should create an environment named `cs410_hw1`. Activate it using `conda activate cs410_hw1`.
1. Then navigate to your projects directory (or create one) and then do `git clone [TODO: ADD URL]`
1. `cd` into the `assignment1` folder 
1. Now install the conda packages required for your system. On my windows systems the required packages are `pip`, `nodejs`, and `pywin32`. This may vary on Linux and Mac machines (i.e you shouldn't need `pywin32`). To install the packages on a windows machine use the following command: `conda install pip nodejs pywin32 --yes`
1. Now install the required pip packages using: `pip install -r requirements.txt`
1. Finally enable the __jupyter lab pyplot widgets__:
    - `jupyter nbextension enable --py widgetsnbextension`
    - `jupyter labextension install @jupyter-widgets/jupyterlab-manager`
1. Now run the notebook using: `jupyter lab`
1. Then open the browser using the link displayed in the output of the jupyter lab command 
or open your browser and go to `http://localhost:8888`, you'll have to paste the token from the output. 

For convenience, here are all the commands
```
conda create -n cs410_hw1 --yes
conda activate cs410_hw1

# Create your project folder and clone the assignment repo
mkdir projects
cd projects
git clone https://gitlab.cs.nuim.ie/cs410_2021/assignment1
cd cs410_hw1

# Note pywin32 should only be required if you are running on a Windows machine
conda install pip nodejs pywin32 --yes
pip install -r requirements.txt

jupyter nbextension enable --py widgetsnbextension
jupyter labextension install @jupyter-widgets/jupyterlab-manager

jupyter lab
```

## Getting familiar with notebooks

For learning purposes, we suggest you create a new notebook and try out some basic python commands.

Notebooks are made up of cells. There are two modes
- Command Mode <kbd>Esc</kbd> (text cursor is not visible, for executing shortcuts)
- Cell Mode <kbd>Enter</kbd> (text cursor is visible, for typing code)

The following shortcuts are the most used ones and can be executed from any mode.
Run Cell Ctrl Enter
Run Cell and go to next cell Shift Enter

You can also search for actions on the sidebar when you press <kbd>Crtl</kbd><kbd>Shift</kbd><kbd>C</kbd> 
and then execute, for example, `Run all cells`

Commands like `Cut` `Copy` `Paste` for _text_ works usual inside text mode once text is selected.
Commands for `Cut` `Copy` `Paste` for _cells_ work when you are on Command Mode
with <kbd>X</kbd>, <kbd>C</kbd> and <kbd>V</kbd> respectively
 
Also, in command mode, insert new cell above with <kbd>A</kbd> and below with <kbd>B</kbd> doing any rough calculations. 
Once you are done, you can delete the current cell with <kbd>D</kbd><kbd>D</kbd> (again, in command mode) 
 
Video Tutorial below
 
[![Jupyterlab Tutorial Video](https://i.imgur.com/jkiUkN7.png)](https://youtu.be/pxirOmilQ3A)
 
If you feel even more adventurous, you can read more [here](https://jupyterlab.readthedocs.io/en/stable/user/interface.html#keyboard-shortcuts).
 
 

## Coding and Submission guidelines

- Open [Assignment1.ipynb](Assignment1.ipynb)
- Read the instructions and fill out necessary code.
- Before submission `Restart Kernel and Run All Cells`, 
check if all cells got executed with output and save the notebook.

You should submit your work as a by saving and uploading your completed [Assignment1.ipynb](Assignment1.ipynb) file through 
the [moodle submision link](https://moodle.maynoothuniversity.ie/mod/assign/view.php?id=247137). When submitting, ensure that you
- do not have cells that display outputs more than a page long, for e.g. printing out all elements of an image array.
- have not added external files or loaded them in the notebook, other than those loaded in the original notebook (i.e. `data.txt`).
- have not used any other libraries/code that provide functionality to produce desired output. e.g. `from skimage.measure import ransac`

## Troubleshooting

- `conda create` fails on Windows. _Solution_: It may fail if you use a normal command prompt. Use _Anaconda Prompt_.
- `pip` is not recognised as an internal or external command. _Solution_: Run `conda install pip -y` in your environment.
- You get an error regarding the fact that `Node.js` is not installed when running `jupyter lab`. _Solution_: Install the nodejs package using `conda`. Run `conda install nodejs`. 

