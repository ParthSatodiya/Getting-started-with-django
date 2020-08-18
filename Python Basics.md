This will cover few keywords around Python language to get you started with basic development.

There are two main versions of Python. Python *2.x* and Python *3.x*. From 2020, Python *2.x* is not supported anymore ([more](https://www.python.org/doc/sunset-python-2/)). So we will be using Python *3.x*.

### :point_right: Installation
Some OS are already come with the python installed. You can check it by running `python --version` in the command line tool. Which will show you the current version of python installed. It can be possible that both Python *2.x* and Python *3.x* is installed simultaneously.In that case, it is most likely that `python` command will execute python *2.x* and `python3` will execute python *3.x*.

If Python *3.x* is not installed on your system then this [link](https://wiki.python.org/moin/BeginnersGuide/Download) will guide you through the installation process for the different platforms. Choose the latest stable version of Python *3.x*.

### :point_right: Before starting
Python already comes with the necessary libraries. But to install any additional libraries, we have a popular package manager called **pip** which we can use. Pip normally included in the Python installation package. You can check it by running `pip` in command line tool. (If both Python versions (*2.x* and *3.x*) are installed then for Python *3.x*, use `pip3` command). If not installed then follow this [link](https://pip.pypa.io/en/stable/installing/).

Different Python projects have a different library or library version requirements. For example if we have two Python projects and both uses different version of django library then it is not possible to install different versions in the same environment. Here we can use the virtualenv which isolates runtime environment for different Python projects. So Python dependency installed in one environment does not interfere with other project environment.

Run `python -m venv /path/to/new/virtual/environment` (or `python3 ...`depending on which keyword used for python *3.x* in your case) which will create an virtual environment at the given path. Then you can follow this [link](https://docs.python.org/3/tutorial/venv.html) to learn how to activate and deactivate this new environment and installing packages in it using pip.

There are some other alternatives also exists which provide both package management and environment management in a single tool. For example [conda](https://conda.io/en/latest/), [pyenv](https://pipenv.pypa.io/en/latest/) etc. Here, we will continue using `pip` for package management. For the virtualization, running Python projects in a container (eg. Docker) is also an option.

### :point_right: Quick concepts
Below provided some links to the official [Python tutorial](https://docs.python.org/3/tutorial/) which will cover main concepts which are being used in daily Python development. Fill free to explore other topics if you want.

* [Number, string and list using Python interactive shell mode](https://docs.python.org/3/tutorial/introduction.html#using-python-as-a-calculator)
* [Control flow tools](https://docs.python.org/3/tutorial/controlflow.html)
* Data structures
    * [Tuples and Sequences](https://docs.python.org/3/tutorial/datastructures.html#tuples-and-sequences)
    * [Sets](https://docs.python.org/3/tutorial/datastructures.html#sets)
    * [Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)
    * [Looping](https://docs.python.org/3/tutorial/datastructures.html#looping-techniques)