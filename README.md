# Python Cheatsheet [![My Skills](https://skillicons.dev/icons?i=py&theme=dark)](https://skillicons.dev)

Welcome to the Python Cheatsheet repository! This repository serves as a comprehensive reference guide for Python, covering the core language features, syntax, standard libraries, and common programming patterns. Whether you're a beginner learning Python or an experienced developer seeking a quick reference, this cheatsheet is here to assist you.

The cheatsheet includes various sections dedicated to Python fundamentals, data types, control flow, functions, modules, file I/O, exceptions, object-oriented programming, regular expressions, and more. Each section provides concise explanations and code examples to help you grasp Python concepts and write clean and efficient code.

Feel free to explore this cheatsheet to enhance your Python skills, automate tasks, build applications, or delve into data science and machine learning. The cheatsheet is written in Markdown format, making it easy to view, copy, and paste into your own projects.

If you have any suggestions or would like to contribute to this cheatsheet, please feel free to open an issue or submit a pull request. Let's collaborate and make this cheatsheet a valuable resource for the Python developer community!

Happy coding with Python!

***

## Table of Contents

1. [About](#about)
2. [Uses](#uses)
3. [Installation](#installation)
4. [Dependencies and Creating a requirements File](#dependencies-and-creating-a-requirements-file)
5. [Syntax](#syntax)
6. [Variables](#variables)
7. [Data Types](#data-types)
   - [Numbers](#numbers)
   - [Strings](#strings)
   - [Booleans](#booleans)
8. [Operators](#operators)
9. [Conditions](#conditions)
10. [Control Flow Statements](#control-flow-statements)
    - [IF](#if)
    - [ELIF](#elif)
    - [WHILE](#while)
    - [FOR](#for)
    - [ELSE](#else)
11. [Collections](#collections)
    - [Lists](#lists)
    - [Tuples](#tuples)
    - [Sets](#sets)
    - [Dictionaries](#dictionaries)
12. [Functions](#functions)
13. [Lambda Functions](#lambda-functions)
14. [List Comprehensions](#list-comprehensions)
15. [Error Handling (try-except)](#error-handling-try-except)
16. [Object-Oriented Programming (OOP) Concepts](#object-oriented-programming-oop-concepts)
    - [Inheritance](#inheritance)
    - [Encapsulation](#encapsulation)
    - [Polymorphism](#polymorphism)
17. [Decorators](#decorators)
18. [Generators](#generators)
19. [File Handling](#file-handling)
    - [Read Files](#read-files)
    - [Write/Create Files](#write-create-files)
    - [Delete Files](#delete-files)
    - [File I/O Modes](#file-io-modes)
20. [Regular Expressions](#regular-expressions)
21. [Date and Time](#date-and-time)
22. [JSON Handling](#json-handling)
23. [CSV Handling](#csv-handling)
24. [Exception Hierarchy](#exception-hierarchy)
25. [Virtual Environments](#virtual-environments)
26. [Package Installation with pip](#package-installation-with-pip)
27. [Command-Line Arguments](#command-line-arguments)
28. [Multithreading](#multithreading)
29. [Multiprocessing](#multiprocessing)
30. [Context Managers (with statement)](#context-managers-with-statement)
31. [Recursion](#recursion)
32. [Web Scraping](#web-scraping)
33. [Data Serialization (e.g., Pickle)](#data-serialization-eg-pickle)
34. [Database Connectivity (e.g., SQLite, MySQL)](#database-connectivity-eg-sqlite-mysql)
35. [Set Methods](#set-methods)
36. [Mathematical Functions (math module)](#mathematical-functions-math-module)
37. [Random Number Generation (random module)](#random-number-generation-random-module)
38. [Working with Files and Directories (os module)](#working-with-files-and-directories-os-module)
39. [Command Execution (subprocess module)](#command-execution-subprocess-module)
40. [Regular Expression Operations (re module)](#regular-expression-operations-re-module)
41. [Handling Dates and Times (datetime module)](#handling-dates-and-times-datetime-module)
42. [Working with CSV Files (csv module)](#working-with-csv-files-csv-module)
43. [Working with JSON Data (json module)](#working-with-json-data-json-module)
44. [Data Compression and Archiving (zipfile module)](#data-compression-and-archiving-zipfile-module)
45. [Networking and Internet Communication (socket module)](#networking-and-internet-communication-socket-module)
46. [Sending Emails (smtplib module)](#sending-emails-smtplib-module)
47. [Web Development (Flask, Django)](#web-development-flask-django)
48. [Scraping Websites (BeautifulSoup, Scrapy)](#scraping-websites-beautifulsoup-scrapy)
49. [Data Visualization (Matplotlib, Seaborn)](#data-visualization-matplotlib-seaborn)
50. [Scientific Computing (NumPy, SciPy)](#scientific-computing-numpy-scipy)
51. [Machine Learning (scikit-learn, TensorFlow)](#machine-learning-scikit-learn-tensorflow)
52. [Data Analysis and Manipulation (pandas)](#data-analysis-and-manipulation-pandas)
53. [Working with Images (PIL/Pillow module)](#working-with-images-pilpillow-module)
54. [GUI Development (tkinter, PyQt)](#gui-development-tkinter-pyqt)
55. [Unit Testing (unittest module)](#unit-testing-unittest-module)


### Dependencies and Creating a requirements File

You should create a `requirements.txt` file for your Python project as soon as you start adding external dependencies to your project. This ensures that you maintain a record of the specific packages and their versions that your project depends on. Here are some guidelines on when to create a `requirements.txt` file:

**When You Add External Packages:**
As soon as you start using external Python packages in your project, it's a good idea to create a `requirements.txt` file. This helps you keep track of the dependencies and their versions, making it easier to recreate the same development environment later.

**When Collaborating with Others:**
If you're collaborating with other developers, a `requirements.txt` file becomes even more important. It ensures that everyone working on the project is using the same set of dependencies, reducing the chances of compatibility issues.

**Before Deploying or Sharing Your Code:**
Before deploying your project to production or sharing it with others, you should update your `requirements.txt` file to include all the necessary dependencies. This ensures that others can set up the same environment and run your code without any issues.

**Regular Maintenance:**
It's a good practice to update your `requirements.txt` file whenever you add, update, or remove dependencies. This keeps the file accurate and up to date with the current state of your project's dependencies.

**Using Virtual Environments:**
If you're using virtual environments (which is recommended), it's a good idea to create a `requirements.txt` file as soon as you've set up your virtual environment and installed the necessary packages within that environment.

In essence, creating a `requirements.txt` file early in your project's development helps establish good practices and ensures that you have a clear record of your project's dependencies. This makes it easier to manage the development, collaboration, and deployment of your Python project.

**Using `requirements.txt` to Install Dependencies:**
Once you have a `requirements.txt` file listing all the required packages and their versions, you can easily set up your development environment on another system by following these steps:

1. **Create a Virtual Environment (Recommended):**
    ```bash
    python -m venv .venv
    source .venv/bin/activate   # On macOS and Linux
    .\venv\Scripts\activate    # On Windows
    ```

2. **Install Dependencies from `requirements.txt`:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Verify Installed Packages:**
    After installation, you can verify that the packages are installed by running:
    ```bash
    pip list
    ```

4. **Deactivate the Virtual Environment:**
    When you're done working with your project, you can deactivate the virtual environment:
    ```bash
    deactivate
    ```

Using the `requirements.txt` file in this way helps ensure that your development environment matches the one you used to develop your project. It's a convenient method to set up and manage dependencies, especially when sharing your code with others or deploying it to different systems.

Remember to keep your `requirements.txt` file up to date as you add or modify dependencies during the course of your project's development.




### Virtual Environments

Setting up new projects within a folder called "Coding" on your desktop and using a virtual environment for each project is a good practice in software development. This approach helps keep your projects organized, isolated, and prevents dependency conflicts between different projects. Here's a step-by-step guide on how to achieve this:

1. Create a Folder on Desktop:

   1.1. Right-click on your desktop and select "New" > "Folder".
   
   1.2. Name the folder "Coding" or any other suitable name you prefer.

3. Set Up New Projects:

   2.1. Open the "Coding" folder you just created.
   
   2.2. Create a new subfolder for each project. Name these subfolders based on your project names (e.g., "ProjectA," "ProjectB").

5. Virtual Environments:

   A virtual environment is an isolated environment for Python projects that allows you to manage dependencies separately for each project. Follow these steps to set up a virtual environment for each project:

   3.1. Open a command-line interface (Terminal, Command Prompt, etc.).

   3.2. Navigate to the directory of your project within the "Coding" folder:

   ``` bash
   cd path\to\Desktop\Coding\ProjectA
   ```
   3.3. Create a virtual environment for your project:

   ``` bash
   python -m venv <name_of_virtual_environment>
   ```
   Common convention is to name your virtual environment .venv
   ``` bash
   python -m venv .venv
   ```
   
   3.4. Activate the virtual environment:

   On Windows:
   ``` bash 
   .venv\Scripts\activate
   ```
   (NOTE: replace ".venv" with your virtual environments name if you have chosen something other than the common convention naming)
   
   On macOS and Linux:
   
   ``` bash
   source .venv/bin/activate
   ```
   3.5. You'll notice that the command prompt changes, indicating that you're now within the virtual environment.

   3.6. Install project-specific dependencies within this virtual environment using pip:

   ``` bash
   pip install package-name
   ```
   3.7 To deactivate the virtual environment when you're done working on the project, simply enter:
   
   ``` bash
   deactivate
   ```
7. Repeat for Each Project:

   Repeat steps 3.2 to 3.7 for each new project you create within the "Coding" folder. Each project will have its own isolated environment and dependencies.

8. Working with Projects:

   8.1. Whenever you want to work on a specific project, navigate to its folder and activate its virtual environment as shown in step 3.4.

   8.2. When you switch between projects, deactivate the current virtual environment (step 3.7) before activating the new one.

By following these steps, you ensure that each project has its own isolated environment, preventing dependency clashes and making it easier to manage and collaborate on multiple projects within the "Coding" folder on your desktop.
