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
    * [List comprehensions](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions)
    * [Tuples and Sequences](https://docs.python.org/3/tutorial/datastructures.html#tuples-and-sequences)
    * [Sets](https://docs.python.org/3/tutorial/datastructures.html#sets)
    * [Dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)
    * [Looping](https://docs.python.org/3/tutorial/datastructures.html#looping-techniques)
* [Errors and Exceptions](https://docs.python.org/3/tutorial/errors.html)
* Classes
    * [A First Look at Classes](https://docs.python.org/3/tutorial/classes.html#a-first-look-at-classes)
    * [Inheritance](https://docs.python.org/3/tutorial/classes.html#inheritance)
* Standard Libraries
    * Dates and Times
        * [timedelta Objects](https://docs.python.org/3/library/datetime.html#timedelta-objects)
        * [date Objects](https://docs.python.org/3/library/datetime.html#date-objects)
        * [datetime Objects](https://docs.python.org/3/library/datetime.html#datetime-objects)
        * [timezone Objects](https://docs.python.org/3/library/datetime.html#timezone-objects)

:point_right: Koans

Koans are puzzles or exercises that are a way to reinforce your learnings of a programming language’s constructs.
The above links to the official docs are best learnt interactively using [koans](https://github.com/gregmalcolm/python_koans).
These are koans in the form of a failing tests that needs fixing as you go. So steps to follow are:
* Follow along with test cases.
* Read through the python official docs regarding the concept being introduced by test.
* Try it out in the python3 REPL.
* Do the necessary edits in test focusing on making concept focused test pass.
* Read more about how python official docs describes it.

### :point_right: CMD Exercise (Simple TODO list)
Build an TODO command line app which will keep track of the new TODO list, mark any finished tasks or update the tasks.
Keep track of the date_updated, date_created and date_finished for every tasks. At the end, we will be able to see tasks list with all the related dates and also the time taken to complete a particular task. All the date-time related calculation should be used along with timezone. So datetime Python library will be used here.

Initially after running the Python program, we will ask basic user information like *username* *timezone of the user*.

Then we can show an empty list of tasks with (Sr no., Task name, Date created) fields and show a list of actions that user can perform.

Actions to show: 
1. Add
2. Update
3. complete
4. Change timezone
5. Completed tasks

After every action completed, we will show all pending tasks with the above list format.

1. Add -> Ask for the task name.
2. Update -> Ask sr no. and ask updated task name.
3. Completed -> Ask sr no.
4. Change timezone -> Ask for the timezone shorthand.
5. Completed tasks -> This will show completed tasks in the below format.

Sr no. | Task name | Date created | Finished at | Time taken
-------|-----------|--------------|-------------|------------|
1 | Glossary | 08/09/2020 11:30 | 08/09/2020 12:45 | 1 h 15 min 
