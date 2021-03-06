Here are my answers to Project 1.

1. A package is the name for a library of code that can be installed, while a library is a collection of functions that can be run after being installed. To install libraries of functions, you need to go to the package manager, which can be found at: File > Settings > Project > Python Interpreter, where you will find a list of the current libraries you have and can upgrade them or install a new one. You can install one by pressing the "+" icon at the bottom of your screen. To make it usable on your script, you need to write "import," followed by the name of your function. You can also give it an abbreviated name in your script by importing it "as" (alias). For example, we had to install pandas and numpy by going to the package manager and installing them, and can now use them in scripts by writing "import pandas as pd" and "import numpy" respectively. Using an alias, such as "pd" for pandas allows you to save space when calling it later in your script.

2. Data frames are essentially tables of data that a Python program can store, with rows representing features that have data associated and columns representing attributes of the data. Pandas is the library that allows programmers to create, edit and print the results from data frames. We can read files from remote locations by writing "path_to_data = " (file name). You can also use the read function to add the data to a variable in your program; you would do this by declaring the variable and setting it equal to "pandas.read_CSV(path_to_data, sep = '\t"). If data is stored in a different file type, you will need to convert it. We have worked extensively with data frames in this class, such as those displaying covid data. If you write a line of code that says the name of your data frame, plus ".shape," the computer will return the number of rows and columns in the table. Shape appears to be the only other terminology for rows and columns, at least for now.

3. Yes, data is displayed every 5 years, starting with 1952. It ends with 2007, so to make it more up to date, we would have to add data from 2012 and 2017.

4. The lowest life expectancy on the table was from Rwanda in 1992. At the time, the life expectancy was just 23.599 years, almost certainly due to high infant mortality.

5. ![image](https://user-images.githubusercontent.com/78311527/112390916-6d9b2300-8ccd-11eb-8d81-3b73844fb610.png)

6.

+ == is used for testing whether two expressions are equal in value. For example, if I executed a line of code that reads "1+1==2" the result will be true because 1 + 1 does in fact equal 2.
+ & means "and" in boolean. For example, if I executed a line of code that reads "(1+1==2) & (1+1==3)" the result will be false because only one of those statements is true. 
+ | means "or" in boolean. For example, if I executed a line of code that reads "(1+1==2) | (1+1==3)" the result will be true because the first of those statements is true.
+ ^ means "not" in boolean. For example, if I executed a line of code that reads "(1+1==2) ^ (1+1==3)" the result will be true because 1 + 1 is 2 and not 3.

7. loc is based on labels, so you would use it to find rows and columns based on their names, whereas iloc is based on integers, which means you would use it to find rows and columns based on their index. Both functions can be used to find multiple rows or columns at once- you would enter the range you wanted to look up.

8. An API is an Application Programing Interface, and is used to collect and process data. As I understand it, constructing a request to a remote server to pull data, write it to a local file and then import it works the same way as reading files, as explained in question 2: "We can read files from remote locations by writing "path_to_data = " (file name). You can also use the read function to add the data to a variable in your program; you would do this by declaring the variable and setting it equal to "pandas.read_CSV(path_to_data, sep = '\t")."

9. Apply, or lamda, refers to anonymous functions, which are those used only once. It's an alternative to more permanent functions and is useful in that it requires much less code to implement, making it a good option if you only need to execute it once.

10. You can specify which specific rows and columns you want to duplicate when making a copy of a data frame. It's common to make copies that only actually include some of the original data to make it easier to work with, without deleting the original data, should you want to look at it again.
