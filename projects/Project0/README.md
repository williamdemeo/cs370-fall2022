# CS 370: Introduction to Artificial Intelligence, Spring 2022

# Project 0. Python setup & autograder tutorial

## Introduction

The projects for this class assume you use Python 3.6.

Project 0 will cover the following:

+ Instructions on how to set up the right Python version,

+ Workflow examples,

+ A mini-Python tutorial,

+ Project grading: Every project's release includes its autograder for you to run yourself.

**Files to Edit and Submit**. During the assignment you will fill in portions of the files `addition.py`, `buyLotsOfFruit.py`, and `shopSmart.py`, which are included in the [tutorial.zip][] archive.  When you are finished solving the coding challenges, you will upload your edited versions of these three files to Gradescope.

**Evaluation**. Your code will be autograded for technical correctness. 

Please *do not* change the names of any provided functions or classes within the code, or you will wreak havoc on the autograder. 
However, the correctness of your implementation---not the autograder's judgements---will be the final judge of your score. 
If necessary, we will review and grade assignments individually to ensure that you receive due credit for your work.

**Academic Dishonesty**. We will be checking your code against other submissions in the class for logical redundancy. 
If you copy someone else's code and submit it with minor changes, we will know. These cheat detectors are quite hard 
to fool, so please don't try. We trust you all to submit your own work only; *please* don't let us down. If you do, we 
will pursue the strongest consequences available to us.

**Getting Help:** You are not alone! If you find yourself stuck on something, contact the course instructor for help. 
Office hours and the discussion forum are there for your support; please use them. If you can't make our office hours, 
let us know and we will schedule more. We want these projects to be rewarding and instructional, not frustrating and 
demoralizing. But, we don't know when or how to help unless you ask.

**Discussion:** Please be careful not to post spoilers.

## Python Installation

Many of you will not have Python 3.6 already installed on your computers. [Conda][] provides an easy way to manage many 
different environments, each with its own Python versions and dependencies. This allows us to avoid conflicts between our 
preferred Python version and that of other classes. We'll walk through how to set up and use a conda environment.

On Windows, to execute these commands, you need to be in an Anaconda prompt.

Prerequisite: [Anaconda][]. Some of you might have already installed this for use with other classes; if you don't, then please install it through the [Anaconda][] link.

### Creating a Conda Environment

The command for creating a conda environment with Python 3.6 is:

```shell
$ conda create --name <env-name> python=3.6
```

(N.B. The `$` symbol is the shell prompt; it's not part of the command.)

We will name our environment `cs370`, so we run the following command, and press `y` to confirm installing any missing packages.

```shell
$ conda create --name cs370 python=3.6
```

### Entering the Environment

To enter the conda environment that we just created, do the following. Note that the Python version within the environment is 3.6, just what we want. Note: if you have an old Anaconda installation, you will need to use source instead of conda for the below, or for Windows, not type conda at all.

```shell
$ conda activate cs370
(cs370) $ python -V
Python 3.6.6 :: Anaconda, Inc.
```

### Leaving the Environment

Leaving the environment is just as easy.

```shell 
(cs370) $ conda deactivate
$ python -V
```

(should show your system's default python version)

----

## Using the Python Language

If you're new to Python, we recommend familiarizing yourself with the language by following the tutorial instructions at the following url:

[https://inst.eecs.berkeley.edu/~cs188/sp22/project0/#python-basics](https://inst.eecs.berkeley.edu/~cs188/sp22/project0/#python-basics).


## Autograding

To familiarize yourself with the autograder we will use for coding projects in this class, please code, test, and submit on Gradescope the three modified Python (`.py`) files after solving three coding exercises.

First, download all of the files associated with this autograder tutorial as a zip archive: [tutorial.zip][]. Unzip this file and examine its contents:

```shell
$ unzip tutorial.zip
$ cd tutorial
$ ls
addition.py   autograder.py   buyLotsOfFruit.py   grading.py   projectParams.py   shop.py
shopSmart.py   testClasses.py   testParser.py   test_cases   tutorialTestClasses.py
```

This contains a number of files you'll edit or run:

+ `addition.py` source file for question 1
+ `buyLotsOfFruit.py` source file for question 2
+ `shop.py` source file for question 3
+ `shopSmart.py` source file for question 3
+ `autograder.py` autograding script (see below)

You can ignore the other files.

The command `python autograder.py` grades your solution to all three problems. If we run it before editing any files we get a page or two of output:

```shell
$ python autograder.py
Starting on 1-21 at 23:39:51

Question q1
===========
*** FAIL: test_cases/q1/addition1.test
***     add(a, b) must return the sum of a and b
***     student result: "0"
***     correct result: "2"
*** FAIL: test_cases/q1/addition2.test
***     add(a, b) must return the sum of a and b
***     student result: "0"
***     correct result: "5"
*** FAIL: test_cases/q1/addition3.test
***     add(a, b) must return the sum of a and b
***     student result: "0"
***     correct result: "7.9"
*** Tests failed.

### Question q1: 0/1 ###

Question q2
===========
*** FAIL: test_cases/q2/food_price1.test
***     buyLotsOfFruit must compute the correct cost of the order
***     student result: "0.0"
***     correct result: "12.25"
*** FAIL: test_cases/q2/food_price2.test
***     buyLotsOfFruit must compute the correct cost of the order
***     student result: "0.0"
***     correct result: "14.75"
*** FAIL: test_cases/q2/food_price3.test
***     buyLotsOfFruit must compute the correct cost of the order
***     student result: "0.0"
***     correct result: "6.4375"
*** Tests failed.

### Question q2: 0/1 ###

Question q3
===========
Welcome to shop1 fruit shop
Welcome to shop2 fruit shop
*** FAIL: test_cases/q3/select_shop1.test
***     shopSmart(order, shops) must select the cheapest shop
***     student result: "None"
***     correct result: "<FruitShop: shop1>"
Welcome to shop1 fruit shop
Welcome to shop2 fruit shop
*** FAIL: test_cases/q3/select_shop2.test
***     shopSmart(order, shops) must select the cheapest shop
***     student result: "None"
***     correct result: "<FruitShop: shop2>"
Welcome to shop1 fruit shop
Welcome to shop2 fruit shop
Welcome to shop3 fruit shop
*** FAIL: test_cases/q3/select_shop3.test
***     shopSmart(order, shops) must select the cheapest shop
***     student result: "None"
***     correct result: "<FruitShop: shop3>"
*** Tests failed.

### Question q3: 0/1 ###

Finished at 23:39:51

Provisional grades
==================
Question q1: 0/1
Question q2: 0/1
Question q3: 0/1
------------------
Total: 0/3
```

Your grades are NOT yet registered. To register your grades, make sure to follow your instructor's guidelines to receive credit on your project.
 
For each of the three questions, this shows the results of that question's tests, the questions grade, and a final summary at the end. 
Because you haven't yet solved the questions, all the tests fail. As you solve each question you may find some tests pass while other fail. 
When all tests pass for a question, you get full marks.

Looking at the results for question 1, you can see that it has failed three tests with the error message "add(a, b) must return the sum of a and b".
The answer your code gives is always 0, but the correct answer is different. We'll fix that now.

Question 1: Addition

Open the `addition.py` file and look at the definition of `add`:

```python
def add(a, b):
    "Return the sum of a and b"
    "*** YOUR CODE HERE ***"
    return 0
```

The tests called this with `a` and `b` set to different values, but the code always returned zero. Modify this definition to read:

```python
def add(a, b):
    "Return the sum of a and b"
    print("Passed a = %s and b = %s, returning a + b = %s" % (a, b, a + b))
    return a + b
```
Now rerun the autograder (omitting the results for questions 2 and 3):

```shell
$ python autograder.py -q q1
Starting on 1-22 at 23:12:08

Question q1
===========

*** PASS: test_cases/q1/addition1.test
*** 	add(a,b) returns the sum of a and b
*** PASS: test_cases/q1/addition2.test
*** 	add(a,b) returns the sum of a and b
*** PASS: test_cases/q1/addition3.test
*** 	add(a,b) returns the sum of a and b

### Question q1: 1/1 ###


Finished at 23:12:08

Provisional grades
==================
Question q1: 1/1
------------------
Total: 1/1
```
You now pass all tests, getting full marks for question 1. Notice the new lines "Passed a=..." which appear before "*** PASS: ...". These are produced by the print statement in `add`. 
You can use print statements like that to output information useful for debugging.

## Question 2: buyLotsOfFruit function

Implement the `buyLotsOfFruit(orderList)` function in `buyLotsOfFruit.py` which takes a list of `(fruit,numPounds)` tuples and returns the cost of your list. If there is some `fruit` in the list which doesn't appear in `fruitPrices` it should print an error message and return `None`. Please do not change the `fruitPrices` variable.

Run `python autograder.py` until question 2 passes all tests and you get full marks. Each test will confirm that 
`buyLotsOfFruit(orderList)` returns the correct answer given various possible inputs. For example,
`test_cases/q2/food_price1.test` tests whether the cost of `[('apples', 2.0), ('pears', 3.0), ('limes', 4.0)] is 12.25`

## Question 3: shopSmart function

Fill in the function `shopSmart(orderList,fruitShops)` in `shopSmart.py`, which takes an `orderList` (like the kind passed in to `FruitShop.getPriceOfOrder`) and a list of `FruitShop` and returns the `FruitShop` where your order costs the least amount in total. Don't change the file name or variable names, please. Note that we will provide the `shop.py` implementation as a "support" file, so you don't need to submit yours.

Run `python autograder.py` until question 3 passes all tests and you get full marks. Each test will confirm that `shopSmart(orderList,fruitShops)` returns 
the correct answer given various possible inputs. For example, with the following variable definitions:

```python
orders1 = [('apples', 1.0), ('oranges', 3.0)]
orders2 = [('apples', 3.0)]
dir1 = {'apples': 2.0, 'oranges': 1.0}
shop1 =  shop.FruitShop('shop1',dir1)
dir2 = {'apples': 1.0, 'oranges': 5.0}
shop2 = shop.FruitShop('shop2', dir2)
shops = [shop1, shop2]
```

`test_cases/q3/select_shop1.test` tests whether: `shopSmart.shopSmart(orders1, shops) == shop1`

`test_cases/q3/select_shop2.test` tests whether: `shopSmart.shopSmart(orders2, shops) == shop2`

------------------------------------------------------------------------------------------------------

## Submission

In order to submit your project, first run `python autograder.py`. If you are satisfied with your score, then upload the following files to Gradescope: `addition.py`, `buyLotsOfFruit.py`, `shopSmart.py`.

------------------------------------------------------------------------------------------------------

## Attribution

This page and the project it describes were adapted from similar materials at [https://inst.eecs.berkeley.edu/~cs188/sp22/project0/](https://inst.eecs.berkeley.edu/~cs188/sp22/project0/), which the dedicated folks at [ai.berkeley.edu](http://ai.berkeley.edu/home.html) have generously made available for reuse.



[tutorial.zip]: https://github.com/williamdemeo/cs370-spring2022/blob/master/projects/Project0/tutorial.zip
[Conda]: https://docs.conda.io/en/latest/
[Anaconda]: https://docs.anaconda.com/anaconda/install/
