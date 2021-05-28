# Dictionaries and Sets in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Objectives
- Define dictionaries in the Python programming language
- Practice utilizing dictionaries and sets in the Python programming language

## Acknowledgements

Elements of this lab procedure were adapted from materials developed by [Dr. Peter Bui](http://www3.nd.edu/~pbui/) for the [CSE 10101 "Elements of Computing I" course](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/).
- [Reading 06: Dictionaries, Sets](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/reading06.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Janet Davis](https://cs.whitman.edu/~davisj/) for the the [CSC 105 "The Digital Age" course](https://www.cs.grinnell.edu/~davisjan/csc/105/2012S/). 
- [Laboratory: Programming in Python](http://www.cs.grinnell.edu/~davisjan/csc/105/labs/python1.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Corey Pennycuff](https://www3.nd.edu/~cpennycu/) for the [CSE 10101 Elements of Computing (Fall 2019)](https://www3.nd.edu/~cpennycu/2019/fa-CSE10101-CDT30010.html).

Elements of this lab procedure were adapted from materials developed by [Lindsay K. Mattock](http://lindsaymattock.net/) for the the [SLIS 5020 Computing Foundations course](http://lindsaymattock.net/computingfoundations.html). 

# Table of Contents
- [Working With Dictionaries](#working-with-dictionaries)
- [Working With Sets](#working-with-sets)
- [Additional Lab Notebook Questions](#additional-lab-notebook-questions)
- [How to submit this lab (and show your work)](#how-to-submit-this-lab-and-show-your-work)
- [Lab Notebook Questions](#lab-notebook-questions)
  
# Working With Dictionaries

78. Refresh: A dictionary is a mapping between a set of indices (keys) and a set of values. Each key maps to a value. The association of a key and a value is called a key-value pair.

<blockquote>Q13: Create a dictionary on a topic of your choosing. Include at least 7 key-value pairs.
<ol type="a">
 <li>Add new elements to your dictionary.</li>
 <li>Update an element in your dictionary.</li>
 <li>Print a list of all the keys in your dictionary.</li>
 <li>Print a list of all the values in your dictionary.</li>
 </ol>
 </blockquote>
 
# Working With Sets

79. Refresh: A set is an unordered collection of unique objects. Sets are primarily used to see if an object or value is in the collection (membership).

<blockquote>Q14: Create the set <code>s</code> with the following values: <code>[1, 3, 5, 7, 9]</code>
<ol type="a">
  <li>Test to see if the value <code>11</code> is a member of the set.</li>
  <li>Test to see if the value <code>7</code> is a member of the set.</li>
  <li>Add a value to the set.</li>
  <li>Remove a value from the set.</li>
 </ol>
 </blockquote>

# Additional Lab Notebook Questions

<blockquote>Q15: What is the difference between a <code>list</code> and a <code>string</code>? What are some methods you can perform on a <code>list</code> that you can't do with a <code>string</code> (and vice versa)?</blockquote>

<blockquote>Q16: What is the difference between a <code>list</code> and a <code>dict</code>? When would we prefer one over the other?</blockquote>

# How to submit this lab (and show your work)

80. Moving forward, we'll submit lab notebooks as `.py` files. 

81. One option is to have a `.py` file that you use to run code and test programs while working through the lab. When ready to submit the lab notebook, you add comments and remove extraneous materials.

82. Another option is to have an "official" `.py` file that you are using as a lab notebook (separate from your working/testing file). Use comments in Python to note when you are starting a new question (as well as answering a question).
  * Example: `Lab5_Notebook_Walden.py`

83. What gets submitted as the lab notebook is the `Lab5_Notebook_Walden.py` file.
- When in doubt, use comments
- Be sure you are using comments to note what question you're responding to

# Lab Notebook Questions

Q1: In your own words, explain the difference between `print(hello)` and `print(“hello”)`.

Q2: Describe the syntax of the three commands that we just used (steps 10-14) in your own words. What is this code doing? Define the function and method for each example.

Q3: Explain how each of these two programs (steps 15-18) work in your own words.

Q4: Why does `print(2/3)` return `0`? How would you modify your code to return the decimal number? Why?

Q5: Explain concatenation in your own words. Why must we convert numbers to strings in the program above? Refer to this example and the previous example.

Q6: Write a program that converts integer, float, or boolean values to a string, using the `str()` function.

Q7: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.

Q8: Modify the program to have it search for other characters in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?

Q9: Create your own list of strings. Include your list code as part of this question answer. What is the length of your list? What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?

Q10: Using the same list from the previous question, write a program that includes the following steps or components:
<ol type="a">
 <li>Adds a new item to your list</li>
 <li>Deletes an item from your list</li>
 <li>Sorts your list in-place</li>
 <li>Generates a sorted version of your list</li>
 <li>Reverse sorts your list in-place</li>
 <li>Generates a reverse sorted version of your list</li>
 <li>Determines the <code>min</code> and <code>max</code> values for your list</li>
 <li>Selects an list element at random</li>
 <li>Shuffles your list</li>
</ol>

Q11: How would you rewrite the code to include only the even numbers from 1 to 10?

Q12: Create the list `numbers` with the following values: `[[0, 1], [2, 3], [4, 5]]`
<ol type="a">
  <li>What is the second element?</li>
  <li>How would you change 4 to 'four'?</li>
  <li>How would you change 1 to 'one'?</li>
  <li>How would you print out each sub-list (one sub-list per line)?</li>
  <li>How would you print out each number (one number per line)?</li>
 </ol>

Q13: Create a dictionary on a topic of your choosing. Include at least 7 key-value pairs.
<ol type="a">
 <li>Add new elements to your dictionary.</li>
 <li>Update an element in your dictionary.</li>
 <li>Print a list of all the keys in your dictionary.</li>
 <li>Print a list of all the values in your dictionary.</li>
 </ol>

Q14: Create the set `s` with the following values: `[1, 3, 5, 7, 9]`
<ol type="a">
  <li>Test to see if the value <code>11</code> is a member of the set.</li>
  <li>Test to see if the value <code>7</code> is a member of the set.</li>
  <li>Add a value to the set.</li>
  <li>Remove a value from the set.</li>
 </ol>
  
Q15: What is the difference between a `list` and a `string`? What are some methods you can perform on a `list` that you can't do with a `string` (and vice versa)?

Q16: What is the difference between a `list` and a `dict`? When would we prefer one over the other?
