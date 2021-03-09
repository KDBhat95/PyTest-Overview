# PyTest-Overview

Testing any code is beneficial. It increases your confidence that the code you wrote behaves as one would expect it to and also ensures that any changes in the code won’t cause regressions.


PyTest is an open-source testing framework that allows users to write test scripts using python. It helps the user to write simple and scalable test cases for the UI, APIs or databases. The PyTest framework helps users to write tests quickly and keep them maintainable and readable (with no boilerplate code needed).
Let’s dive into more details regarding PyTest and how to use it.

## Benefits of PyTest
The advantages of Pytest are as follows −

1)	Pytest can run multiple tests in parallel, which reduces the execution time of the test suite.

2)	Pytest has its own way to detect the test file and test functions automatically, if not mentioned explicitly.

3)	Pytest allows us to skip a subset of the tests during execution.

4)	Pytest allows us to run a subset of the entire test suite.

## How to use PyTest

### Installing PyTest

To install the latest version of PyTest, execute the following command –

`pip install pytest`

Confirm the installation with the following command – 

`pytest -h`

Now, let’s test our first pytest program. First create a directory and navigate into the directory to create the files.
Let us follow the steps shown below −

•	Create a new directory with any name and navigate into the directory in your command line.

•	Create a file named test_square.py and add the below code to that file.


```
import math

def test_sqrt():
   num = 25
   assert math.sqrt(num) == 5

def testsquare():
   num = 7
   assert 7*7 == 40
```

Run the test with the following command –

`pytest`

The above command will generate the following output –
 
<img src=https://github.com/KDBhat95/PyTest-Overview/blob/main/pytest_img.PNG width=800 /><br>

### How Pytest identifies the test files and test methods

By default, pytest only identifies the file names starting with test_ or ending with _test as the test files. We can explicitly mention other filenames as well. Pytest requires the test method names to start with "test." All other method names will be ignored even if we explicitly ask to run those methods.

Here are some examples of valid and invalid pytest file names - 

```
test_login.py - valid
login_test.py - valid
testlogin.py - invalid
logintest.py - invalid
```

## PyTest: Advanced features
PyTest has 2 main advanced features that can also be used:

*	Fixtures - Fixtures are how test setups (and any other helpers) are shared between tests. While we can use plain functions and variables as helpers, fixtures are super-powered with functionality, including:

    *	The ability to depend on and build on top of each other to model complex functionality.

    *	The ability to customize this functionality by overriding fixtures at various levels.

*	The ability to parametrize (that is, take on multiple values) and magically run every dependent test once for each parameterized value.

## Conclusion
Pytest offers a core set of productivity features to filter and optimize your tests along with a flexible plugin system that extends its value even further. Whether you have a huge legacy unit test suite or you’re starting a new project from scratch, pytest has something to offer you.

## References:
1) [Effective Python Testing with PyTest](https://realpython.com/pytest-python-testing/)
2) [Testing Applications with Pytest](https://semaphoreci.com/community/tutorials/testing-python-applications-with-pytest/)
3) https://docs.pytest.org/en/stable/
4) [5 Pytest Best Practices for Writing Great Python Tests](https://www.nerdwallet.com/blog/engineering/5-pytest-best-practices/)
5) https://www.tutorialspoint.com/pytest/index.htm

## Authors:
Team 9: Angry Nerds- Sowjanya Achar, Meeti Baliga, Krithika Bhat, Anusha Gupta
