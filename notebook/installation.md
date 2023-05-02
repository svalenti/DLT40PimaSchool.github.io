------------------------------------
Installing Miniconda3 under Windows
------------------------------------
Download and run the appropriate installer from:https://docs.conda.io/en/latest/miniconda.html#
If prompted, you should choose to:
1)  Accept the license / terms of use.
2)  Install for just the current user, not all users.
Once installed, check that you can run the "Anaconda Prompt".  
From the prompt, run the command:conda --version

Video to install miniconda on Windows
https://www.youtube.com/watch?v=tXgPY4lc6fo

--------------------------------------------
Installing Miniconda3 under Linux or macOS
--------------------------------------------
Download the appropriate installer for your OS here:https://docs.conda.io/en/latest/miniconda.html#
For macOS, you can choose between a "package" or "bash" version. 
I find it easier to follow the bash version, but the package version will work too. 
I recommend you make the following choices described below.
1)  Accept the license / terms of use.
2)  Do not install for all users, but just the current user.
3)  You might be asked whether or not to allow the installer to issue "conda init".  
Answering "no" will require you to activate conda yourself each time you open a new terminal, 
following the instructions that will be provided during installation.  
Make sure you record these instructions if you choose "no".  
I recommend answering "yes".  This will set some environment variables persistently in 
your shell so that conda is setup every time you open a terminal.  
I recommend "yes", and the remaining instructions assume that you have done so.
During the installation, take note of the installation location of miniconda in your log file.
The default installation should put conda here:  YOUR_HOME_DIRECTORY/opt/miniconda3/

------------------------------------------
Installing PIMA  Conda Environment
------------------------------------------
Make sure your conda is fully up to date with:
conda update conda
then follow the prompts, e.g. selecting "y" as needed to update any out-of-date packages.
We'll be using a conda environment specifically for PIMA school to avoid conflicts 
with any other projects on your computer, and to ensure that we all have the same software installed.  
To create our environment:
conda create -n pima python=3.8 numpy scipy matplotlib ipython jupyter

-------------------------------------------------------------
Starting pima Conda Environment and Jupyter Notebook
-------------------------------------------------------------
Activate the pima python environment with 
conda activate pima 

now we need to install last package: sep

there are two way:
 - conda install -c conda-forge sep 
or
 - pip install sep

Then launch jupyter notebook with:
jupyter notebook
Note that the directory in which you run this command will be the rootdirectory in your jupyter notebook.  
Keep this in mind when you are reading or writing data files!
When you are done with pima for the session you can deactivate the environment with: conda deactivate