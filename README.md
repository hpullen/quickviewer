# QuickViewer package

A package for interactively viewing medical image data.

## Installation

1. Install using [pip](https://pip.pypa.io/en/stable/):
   - Optionally create virtual environment, for example:
     ```
     mkdir test_area
     cd test_area
     virtualenv .
     source bin/activate
     ```
   - With [gitlab access via ssh keys](https://docs.gitlab.com/ee/ssh/):
     ```
     pip install git+ssh://git@codeshare.phy.cam.ac.uk:/hp346/quickviewer
     ```

2. Install using [git](https://git-scm.com) and [conda](https://docs.conda.io/):
   - Clone repository:
     - With [gitlab access via ssh keys](https://docs.gitlab.com/ee/ssh/):
       ```
       git clone --recurse-submodules git@codeshare.phy.cam.ac.uk:/hp346/quickviewer
       ```
     - With [gitlab access via token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html):
       ```
       git clone --recurse-submodules https://codeshare.phy.cam.ac.uk/hp346/quickviewer
       ```
       Note that this may not work with older versions of git.  It has
       been tested successfully with git version 2.21.1.
   - From top-level directory of cloned repository, create **quickviewer**
     environment:
     ```
     conda env create --file environment.yml
     ```
   - Activate **quickviewer** environment:
     ```
     conda activate quickviewer
     ```


## Usage

### In a jupyter notebook:

1. Ensure you are inside an environment that has `quickviewer` installed as a package; if you followed the conda installation method, you can do this by running 
```conda activate quickviewer```
inside a terminal.
2. Launch a jupyter notebook server by running 
```jupyter notebook```
inside the terminal where you activated the environment.
3. Create a new notebook and import the `QuickViewer` class by running:
```from quickviewer import QuickViewer```
4. You can now use the QuickViewer class to create interactive plots in your notebook.

### From the command line:
1. A script for creating a quickviewer plot from the command line can be found in `quickviewer/bin/quick_view.py`. The basic usage for viewing a NIfTI file is:
```quick_view.py <filename>```.
2. To see the available input options for this script, run:
```quick_view.py -h```
3. Running this script will create a figure in a seperate window, which can be interacted with using the following commands:
    - **scroll wheel**: scroll through image one slice at a time
    - **left/right arrows**: scroll through image one slice at a time
    - **up/down arrows**: scroll through image five slices at a time
    - **v**: switch orientation
    - **d**: change dose field opacity
    - **m**: turn masks on and off
    - **c**: toggle structure plotting type between contours, masks, and none
    - **j**: jump between the structures on the image
    - **i**: invert any comparison images
    - **o**: change the opacity of overlay comparison image

### Inside a python script:
The `QuickViewer` class can be imported into a python script by adding
```from quickviewer import QuickViewer```
to the script. Creating a `QuickViewer` object inside the code will cause a window containing the plot to be opened when the code is run.
