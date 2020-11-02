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

### :point_right: Exercise 1

Given the cow milkings array and the collection array, find out how many milkings happened for each collection.
Both arrays are sorted based on the date and time. Use Python datetime library if required.

- Sample input:
```
6
12/03/2020 03:00
12/03/2020 15:00
13/03/2020 15:00
14/03/2020 06:00
15/03/2020 12:00
16/03/2020 03:30
3
12/03/2020 16:00
14/03/2020 16:30
16/03/2020 05:00
```

- Sample output:
```
{
    "12/03/2020 16:00": 2,
    "14/03/2020 16:30": 2,
    "16/03/2020 05:00": 2
}
```

### :point_right: Exercise 2 (Simple TODO list)
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

### :point_right: Exercise 3 (OOP using Chess movement simulator)

You are required to create a program, which simulates a chessboard and the
movements of various types of pieces on the chessboard.

*Chessboard*:

The chessboard is an 8 x 8 grid with 64 cells in it.
With 8 rows (A, B, C.... H) and 8 columns (1, 2, 3.... 8), each cell can be uniquely
identified with its cell number. This can be seen illustrated below.

```
A1 A2 A3 A4 A5 A6 A7 A8  
B1 B2 B3 B4 B5 B6 B7 B8  
C1 C2 C3 C4 C5 C6 C7 C8  
D1 D2 D3 D4 D5 D6 D7 D8  
E1 E2 E3 E4 E5 E6 E7 E8  
F1 F2 F3 F4 F5 F6 F7 F8  
G1 G2 G3 G4 G5 G6 G7 G8  
H1 H2 H3 H4 H5 H6 H7 H8
```

Chess pieces and their movements:
The game of chess has 6 unique types of pieces, with their own unique types of movements. These are:
* King – Can move only 1 step at a time in all 8 directions (horizontal, vertical
and diagonal)
* Queen – Can move across the board in all 8 directions
* Bishop – Can move across the board only diagonally
* Horse – Can move across the board only in 2.5 steps (2 vertical steps and 1
horizontal step)
* Rook – Can move across the board only vertically and horizontally
* Pawn – Can move only 1 step at a time, in the forward direction, vertically.
Can also move 1 step forward diagonally, in order to eliminate an opposing
piece.

*Assumption*:
Assume that the board is empty. This means that the pawn cannot move
diagonally and no considerations are needed for another piece already occupying next cell.

*Sample run*:

```
./chess.py King E3
E2, E4, D3, F3, D2, F2, D4, F4
./chess.py Queen E3
E2, E1, E4, E5, E6, E7, E8, D3, C3, B3, A3, F3, G3, H3, D2, C1, F2, G1, D4, C5, B6, A7, F4, G5, H6
./chess.py Bishop E3
D2, C1, F2, G1, D4, C5, B6, A7, F4, G5, H6
./chess.py Rook E3
E2, E1, E4, E5, E6, E7, E8, D3, C3, B3, A3, F3, G3, H3
./chess.py Pawn E3
D3, F3
./chess.py Horse E3
D1, F1, D5, F5, C2, C4, G2, G4
```

*Suggested roadmap*:
1. Design piece which can move horizontally on any grid (8 X 8, 2 X 3) limited by its allowed steps.
2. Design piece which can move vertically on any grid limited by its allowed steps.
3. Design piece which can move diagonally on any grid limited by its allowed steps.
4. Design special piece having multiple movements in different directions.
5. Mix pieces that can move in multiple direction to form one of the above.


### :point_right: Exercise 4 (Simple list/dictionary and file operations)
You have to read and parse json files and perform below actions.
All the necessary information for how to handle JSON files in python is given in [this article](https://www.programiz.com/python-programming/json).

#### Sum and frequency
Create a json file with the format given below and perform the following exercises.
```json
[1, 56, -80, 23, 52, 12, 43, 8, -80, 56, 52]
```

1. Print the total of all the numbers. So the output would be a single integer number
2. Print the frequency of all different numbers. So the output would be a dictionary with all unique numbers given in the json file as keys and it's respective frequency as values.
For example,
```
{
    1: 1,
    56: 2,
    ...
}
```
3. Try to create two JSON output file named `sum.json` and `freq.json` with the result of the respective exercise.

#### Get useful information from the transaction log
Create a json file with the format given below and perform the following exercises. (You can modify the data to simulate every possible cases)
```json
{
	"users": [
		{
			"acc_id": "101",
			"name": "bob",
			"current_balance": 24000
		},
		{
			"acc_id": "102",
			"name": "alice",
			"current_balance": 30000
		},
		{
			"acc_id": "105",
			"name": "arjun",
			"current_balance": 35000
		}
	],
	"bank_transactions": [
		{
			"acc_id": "101",
			"date": "12/10/2020 03:00",
			"amount": 2000,
			"type": "debit"
		},
		{
			"acc_id": "102",
			"date": "15/10/2020 03:00",
			"amount": 200,
			"type": "debit"
		},
		{
			"acc_id": "101",
			"date": "15/10/2020 13:00",
			"amount": 5000,
			"type": "credit"
		},
		{
			"acc_id": "105",
			"date": "20/10/2020 03:00",
			"amount": 2000,
			"type": "credit"
		}	
	]
}
```

1. Accept account_id shell input from user and give total number of transactions performed on that account. So the output would be a single integer number.
2. Print dictionary where account_ids as keys and current bank balance of that account after performing all bank transactions as values.
For example,
```
{
    "101": 27000,
    "102": 29800,
    "105": 37000
}
```

#### Handle amount transfer within a bank
Create a json file with the format given below and perform the following exercises. (You can modify the data to simulate every possible cases)
```json
{
	"users": [
		{
			"acc_id": "101",
			"name": "bob",
			"current_balance": 24000
		},
		{
			"acc_id": "102",
			"name": "alice",
			"current_balance": 30000
		},
		{
			"acc_id": "105",
			"name": "arjun",
			"current_balance": 35000
		}
	],
	"bank_transfers": [
		{
			"from_account_id": "101",
			"to_account_id": "102",
			"amount": 200,
			"date": "23/10/2020 03:00"
		}
		...
	]
}
```

1. Implement bank transfer functionality. So a bank user should be able to transfer amount to other person's bank account.
	- Accept "from account id", "to account id", "amount to transfer" as the shell input.
	- Print dictionary with account_ids as keys and respective current_balance as values.
2. After each transfer, update input JSON file with `current_balance` of the related user accounts and log the transfer in the `bank_transfers` array given in the input file with the same format. So initially that array is empty. Now whenever you execute the code, it will update the `current_balance` of the related user accounts and also add new entry in the `bank_transfer` array. Now the next code execution will use this updated JSON file. `date` in each transfer log object is the date time when the transfer occurred.
3. Use the data given in the input JSON file. Now each items given in the `bank_transfers` array is not yet applied on the user accounts. So you have to simulate each transfer on the users and update the `current_balance` accordingly. Here the `bank_transfers` array can not be sorted based on the datetime so make sure you perform each transfer in order.
- For each users, you have to keep track of how many debits or credits occurred and how many invalid transfers happened for a particular user.
whenever invalid transfer identified, you should avoid that for updating `current_balance` for the related users.
- You should cover all the required cased in your input JSON file.
- Expected output structure:
	```json
	{
		"101": {
			"credits": 12,
			"debits": 13,
			"invalid_transfer": ["23/10/2020 03:00"],
			"current_balance": 2300
		}
		...
	}
	```

#### File listing and grouping
Ask for the directory path as a shell input, validate that path; whether it's exists in the system, whether it's a directory path or not.
1. List all files in that directory, group by extension and give the total size per group (use regex if possible to extract extensions from the file names). For now, ignore nested directories in the given path. The output would be a dictionary with file extension as keys and total size of that extension as values.
For using regex in Python, refer [this article](https://www.programiz.com/python-programming/regex).

#### Product sales
Given the list of products with total sales per products,
```json
[
	{
		"name": "A",
		"price": 12,
		"currency": "euro",
    	"totalSales": 12000
	},
	...
]
```
1. Calculate for each product the percentage of the total sales amount among all products
2. Sort the products from best to worst sales, and calculate the cumulative percentage
So for exercise 2, output will look something like this for the list of 3 products;
```json
[
	{
		"name": "A",
		"totalSales": 10000,
		"percentage": "50%",
		"cumulativePercentage": "50%"
	},
	{
		"name": "C",
		"totalSales": 6000,
		"percentage": "30%",
		"cumulativePercentage": "80%"
	},
	{
		"name": "B",
		"totalSales": 4000,
		"percentage": "20%",
		"cumulativePercentage": "100%"
	}
]
```



