---
layout: post
title: Setting up an Anaconda environment for machine learning and reinforcement learning
---





In this tutorial I walk through the steps required to setup and use Anaconda environment for machine learning (ML) and reinforcement learning (RL) experiments. This tutorial does not assume any power user skills, and is optimized to be understandable to anyone.

Overview
--------

Anaconda Navigator is an easy, point-and-click way to work with packages and environments without needing to use conda commands in a terminal window. You can use it to find the packages you want, install them in an environment, run the packages and update them, all inside Navigator.

The steps I follow to set up the environment are:

  1. [Install Anaconda Navigator.](#installing)
  2. [Create an Anaconda environment.](#create)
  3. [Install the necessary packages.](#package)
      1. Packages in the Anaconda package list: ```numpy```, ```scipy```, ```sklearn```, ```pandas```, ```tensorflow```, ```theano```.
      2. Packages not  in the Anaconda package list: ```keras```, ```gym```.
  4. [Install the tools to use with the environment.](#tools)
  5. [Use the environment.](#use)

Each step is detailed below.

----------

Installing and starting Anaconda Navigator <a name="installing"></a>
------------------
Download and install a version of Anaconda Navigator for your operating system from here: [https://www.continuum.io/downloads](https://www.continuum.io/downloads).

#### macOS:
When you install Anaconda on macOS, a Navigator menu item is automatically added to your programs menu. On macOS you can start Navigator by clicking the Navigator menu item, or by opening a terminal window and running the command anaconda-navigator.

#### Linux:
On Linux you can start Navigator by opening a terminal window and running the command anaconda-navigator. When you install Anaconda on Linux, Anaconda does not add shortcuts automatically because different Linux distributions have different systems for adding menu or desktop shortcuts. You can use your operating system to create desktop and/or main-menu shortcuts that run the command anaconda-navigator.

#### Windows:
When you install Anaconda on Windows, a Navigator menu item is automatically added to your programs menu and an icon is added to your desktop. You can use either to start Navigator.



----------


Creating and activating a new environment <a name="create"></a>
-------------------------------------------------------

To create a new environment: In Navigator, click the Environments tab, then click the Create button.

![]({{ site.baseurl }}/images/conda-tutorial/click-env.PNG)

![]({{ site.baseurl }}/images/conda-tutorial/click-create.PNG)

The Create new environment dialog box appears. In the Environment name field, type a descriptive name for your environment. We’ll create an environment using the newest version of Python, Python 3.6. In the Python version list, select Python 3.6. Click the Create button.

![]({{ site.baseurl }}/images/conda-tutorial/create-env.PNG)

Navigator creates the new environment and activates it, as shown by the highlighted green bar. All actions take place in the active environment.

![]({{ site.baseurl }}/images/conda-tutorial/env-activated.PNG)
----------

Finding and installing a package <a name="package"></a>
--------------------------------

For this example we will install the core packages commonly used for machine learning and reinforcement learning: ```numpy```, ```scipy```, ```sklearn```, ```pandas```, ```tensorflow```, ```keras``` and ```gym```.


There are many ways to install a package into the Anaconda environment; here we cover two of them:
- If the package is contained in the Anaconda package list, it can be installed via Anaconda Navigator itself. Packages ```numpy```, ```scipy```, ```sklearn```, ```pandas```, ```tensorflow```, ```theano``` are all contained in the Anaconda package list.
- If the package is not contained in the Anaconda package list, one can install it into the Anaconda environment with a command line via ```pip```. We will install packages ```gym``` and ```keras``` in this manner.

### Package is in the Anaconda package list ###

In the list at the top left of the packages area, select All. In the Search Packages box, type the name of the package, i e ```numpy```. In the search results, select the checkbox next to the package.

![]({{ site.baseurl }}/images/conda-tutorial/install-numpy.PNG)

In a similar fashion, add more packages (i e ```scipy```, ```sklearn```, ```pandas```, ```tensorflow```) to the to-be-installed list.

In the Install Packages window, review the packages to be installed, then click the Apply button. Then in Navigator, click the Apply button.

![]({{ site.baseurl }}/images/conda-tutorial/click-apply.PNG)

In the confirmation dialog, click the Ok button. All package files and dependencies will be installed in your active environment.

### Package is not in the Anaconda package list ###


Not all python packages are indexed in the Anaconda package list. If you are not able to find a desired package in the list, other means of installation are available. Here is a demonstration of installing packages into the Anaconda environment via ```pip```:

1. Open the Command Prompt and activate the Anaconda environment by entering:  
  - Windows: ```activate ml-rl-env```.
  - macOS and Linux:  ```source activate ml-rl-env```

    In the general case the name of the environment ```ml-rl-env``` is replaced with the name of
    the environment one is working with.

2. Install the packages via pip:
  - Windows: ```pip install gym keras```
  - macOS and Linux:  ```pip3 install gym keras```


Installing the tools to use with the environment <a name="tools"></a>
--------------------

Anaconda Navigator offers an easy, point-and-click way to install multiple tools useful for development and experimenting. For ML and RL experiments one would most likely want to use Spyder and Jupyter notebook. To install these tools:
1. Go to the Home tab of Anaconda Navigator and select the ```ml-rl-env``` environment from the list of environments;
2. Click install for the necessary tools.  

![]({{ site.baseurl }}/images/conda-tutorial/install-tools.PNG)





Using the environment<a name="use"></a>
--------------------

### Jupyter notebook

For using the Jupyter notebook I recommend launching it from the terminal on macOS and Linux and from the Anaconda Prompt on Windows.

#### Linux and macOS:
1. Open the terminal and ```cd``` to your working directory.
2. Activate the Anaconda environment by entering ```source activate ml-rl-env```. Conda prepends the path name ```ml-rl-env``` onto your system command.
3. Launch the Jupyter notebook: enter ```jupyter notebook```

#### Windows:
1. Launch the Anaconda Prompt
2. ```cd``` to your working directory. You can also make a shortcut to open the Anaconda Prompt in the directory you use often.
3. Activate the Anaconda environment by entering ```activate ml-rl-env```
4. Launch the Jupyter notebook: enter ```jupyter notebook```

### Spyder and other applications
On the Home tab of Anaconda Navigator, select the environment name from the drop-down list. The applications installed for
this environment can be launched from here.

![]({{ site.baseurl }}/images/conda-tutorial/use-env.PNG)
