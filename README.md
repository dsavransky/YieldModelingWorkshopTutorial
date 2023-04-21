# Yield Modeling Workshop 2023 Tutorials

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/dsavransky/YieldModelingWorkshopTutorial/HEAD?urlpath=lab/tree/Notebooks){:target="_blank"}

## Running the Tutorials

These tutorials can be run entirely via your browser, with no local installation required.  This is recommended for all beginners and anyone who wants to casually explore the code. Users wishing to install the code on their own computers should use one of the options below.

### The Easy Way (No Local Installation) 

Click the 'launch binder' badge at the top of this readme and wait a few minutes (it may take a while).  Once JupyterLab launches, click on the file browser (top icon in the left-hand panel) and select a notebook (for example, `EXOSIMS_tutorial1.ipynb`).  In order to execute code cells, hit Shift+Enter (or use the Run icon in the toolbar).  You can also execute all cells (or some subset of cells) via options in the Run menu.

### The Slightly Harder Way (Local Installation)

If you are planning on using these tools more extensively, it is recommended that you install them locally on your own machine.  We recommend using a dedicated virtual python environment.  The instructions below assume that you have python (version 3.10 or higher recommended) and pip installed and working on your machine. For help with that, start here: https://wiki.python.org/moin/BeginnersGuide/. We'll assume that python and pip are runnable as `python` and `pip`, respectively, but they might be called `python3` and `pip3` (or something else) on your particular system. These instructions are based on working in a terminal (macOS/Linux) or command prompt/PowerShell (Windows).

1. Download or clone this repository to your computer (https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
2. Create a python virtual environment (we'll call ours `YieldModelingTutorial` but you can replace this with any name you like). In a terminal/command prompt/powershell/etc, navigate to a directory where you want to create the virtual environment and run:
   
   ```python -m venv YieldModelingTutorial```
   
3. Activate the environment. On macOS/Linux (see https://docs.python.org/3/library/venv.html for Windows details):

    ```source YieldModelingTutorial/bin/activate```

4. In the same terminal with the active virtual environment, navigate to the cloned/downloaded repository.  From the top level directory of the repository (the one that contains the file `requirements.txt`) run:

    ```pip install --upgrade -r requirements.txt```
    
    This will install all of the python packages required by the tutorial notebooks.
 
5. Navigate to the `Notebooks` subdirectory of the repository (this should just be `cd Notebooks` from where you were last) and then start JupyterLab by running `jupyter-lab`

6. From this point, everything is the same as via the Easy Way.

7. To stop JupyterLab, type `ctrl+c` in the terminal where it is running and then hit `ctrl+c` again (or type `y` at the prompt). To deactivate the virtual environment just type `deactivate` at the prompt.  Next time you want to run the tutorials again, you just activate the environment again, navigate to the Notebooks directory and run `jupyter-lab`

>**Warning**
>There appears to be an issue (at least on macOS) where if you already have jupyter-lab installed in a system path, it will be executed initially instead of the one you install in your virtual environment.  A simple fix is to deactivate and re-activate the virtual environment after you run the initial pip installation (i.e., between steps 4 and 5).

### Editable Installs 

If you are planning on doing your own development/modification of any of the tools used here, you may wish to create editable (developer) installs.  To do so, you should grab the repositories of the tools themselves.  In the case of `EXOSIMS`, this looks something like:

    git clone https://github.com/dsavransky/EXOSIMS.git
    cd EXOSIMS
    pip install --user -e .

The `-e` flag installs the software in such a way that changes to the repository are automatically picked up the next time the relevant module is reloaded.  This is very convenient for development and testing. 







