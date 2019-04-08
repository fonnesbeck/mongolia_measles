# mongolia_measles
Mongolia measles outbreak intervention modeling

This repository contains work concerned with estimating measles dynamics models for outbreaks in Mongolia, 2015-2016. There are three primary Jupyter notebooks:

- `Confirmation Rates.ipynb`: Development of models for estimating confirmation bias. Methods developed here were implemented in the full measles dynamics model.
- `Data Processing.ipynb`: Steps for cleaning and processing data prior to analysis. The notebook imports data as received and processes it in a reproducible manner, saving the processed versions as CSV files for later use.
- `Measles Dynamics.ipynb`: The main analysis notebook. Uses Bayesian methods to estimate the parameters of an SIR model for the Mongolia outbreaks. Uses the data processed in `Data Processing.ipynb`.

## Running the models

This repository can be cloned and run on your local machine, provided the appropriate Python environment is installed. 

Python comes pre-installed on some systems, but I recommend using the [Anaconda](https://www.anaconda.com/) distribution because it includes enhancements that make configuring and maintaining Python on your computer much easier. Anaconda is freely available from the [Anaconda download page](https://www.anaconda.com/distribution/#download-section).

Download the Python 3.7 installer for your system, and execute the file, following the on-screen instructions.

### System requirements

- Operating system: Windows 7 or newer, 64-bit macOS 10.10+, or Linux, including Ubuntu, RedHat, CentOS 6+, and others.
- If your operating system is older than what is currently supported, you can find older versions of the Anaconda installers in our archive that might work for you.
- System architecture: Windows- 64-bit x86, 32-bit x86; MacOS- 64-bit x86; Linux- 64-bit x86, 64-bit Power8/Power9.
- Minimum 5 GB disk space to download and install.

On Windows, macOS, and Linux, it is best to install Anaconda for the local user, which does not require administrator permissions and is the most robust type of installation.

During the installation, you will be asked if Anaconda should modify the PATH variable on your machine. It is recommended that you allow this, as it permits Anaconda to become the default Python installation on your machine, incase there are other versions already on your system.

### Creating a virtual environment

Once Python is installed, either clone this repository using `git` or download and unzip the zip archive of the project.

The repository fcontains a file called `environment.yml` that includes a list of all the packages used for the analysis. If you run

    conda env create

from the directory containing `environment.yml` it will create the environment for you and install all of the packages listed. This environment is called "mongolia", and it can be activated using:

    conda activate mongolia

### Running the Jupyter notebooks

Having activated the environment, from inside the `notebooks` subdirectory you can start up either a Jupyter notebook instance:

    jupyter notebook

or a JupyterLab instance:

    jupyter lab

This should open Jupyter in your default browser, from which the models may be run.