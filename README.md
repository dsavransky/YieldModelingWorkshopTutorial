# Yield Modeling Workshop 2023 Tutorials

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/dsavransky/YieldModelingWorkshopTutorial/HEAD?urlpath=lab/tree/Notebooks)

## Running the Tutorials

These tutorials can be run entirely via your browser, with no local installation required.  This is recommended for all beginners and anyone who wants to casually explore the code. There are two ways to run the tutorials in the browser: using binder or using Google colab.  Details for launching using both services are provided below.

Users who wish to run the tutorials locally on their own computers, or to develop new implementations for EXOSIMS should install the code locally (see instructions below).

### Easy Way #1: Google Colab (No Local Installation) 

For any of the notebooks in the `colab` subfolder, prepend the url https://colab.research.google.com/github/dsavransky/YieldModelingWorkshopTutorial/blob/main/colab/.  So, for the first tutorial, you would navigate to:

https://colab.research.google.com/github/dsavransky/YieldModelingWorkshopTutorial/blob/main/colab/EXOSIMS_tutorial1_colab.ipynb

If you are not logged in to a google-linked account, you will need to sign in (using the Sign In button at the top right of the screen). Afterwards, you will be able to execute the notebook by placing your cursor in a code cell and hitting Shift+Enter (or use the Run icon in each cell).  You can also execute all cells (or some subset of cells) via options in the `Runtime` menu.


### Easy Way #2: binder (No Local Installation)

>**Warning**
>As of May, 2023 binder has suffered a reduction in capacity (see: https://blog.jupyter.org/mybinder-org-reducing-capacity-c93ccfc6413f), which leads to frequent failures. If binder fails to load, please try the Google colab version, described above.

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







