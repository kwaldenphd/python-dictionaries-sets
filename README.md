# Dictionaries and Sets in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Objectives
- Define dictionaries in the Python programming language
- Practice utilizing dictionaries and sets in the Python programming language
  * For dictionaries, this includes basic syntax, ordering, adding key-value pairs, updating, lists, and iteration
  * For sets, this includes basic syntax, adding and removing, and testing for membership
- Use Python methods and functions to work with dictionaries and sets

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
  <td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=df2efb55-a837-454e-910d-ad820163cda5">Lab overview</a></td>
  </tr>
  </table>
  
<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
<td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?pid=266f95e7-65bd-4718-9a97-ae300135e32a">Lecture/live coding playlist</a></td>
  </tr>
  </table>

## Acknowledgements

Elements of this lab procedure were adapted from materials developed by [Dr. Peter Bui](http://www3.nd.edu/~pbui/) for the [CSE 10101 "Elements of Computing I" course](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/).
- [Reading 06: Dictionaries, Sets](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/reading06.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Janet Davis](https://cs.whitman.edu/~davisj/) for the the [CSC 105 "The Digital Age" course](https://www.cs.grinnell.edu/~davisjan/csc/105/2012S/). 
- [Laboratory: Programming in Python](http://www.cs.grinnell.edu/~davisjan/csc/105/labs/python1.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Corey Pennycuff](https://www3.nd.edu/~cpennycu/) for the [CSE 10101 Elements of Computing (Fall 2019)](https://www3.nd.edu/~cpennycu/2019/fa-CSE10101-CDT30010.html).

Elements of this lab procedure were adapted from materials developed by [Lindsay K. Mattock](http://lindsaymattock.net/) for the the [SLIS 5020 Computing Foundations course](http://lindsaymattock.net/computingfoundations.html). 

# Table of Contents
- [Lecture and Live Coding](#lecture-and-live-coding)
- [Lab Notebook Template](#lab-notebook-template)
- [Dictionaries](#dictionaries)
  * [Creating a Dictionary](#creating-a-dictionary)
  * [Interacting With a Dictionary](#interacting-with-a-dictionary)
  * [Iteration and Dictionaries](#iteration-and-dictionaries)
  * [Dictionary Lab Notebook Question](#dictionary-lab-notebook-question)
- [Sets](#sets)
  * [Creating Sets](#creating-sets)
  * [Testing For Membership](#testing-for-membership)
  * [Adding and Removing Items](#adding-and-removing-items)
  * [Set Lab Notebook Question](#set-lab-notebook-question)
- [Additional Lab Notebook Questions](#additional-lab-notebook-questions)
- [How to submit this lab (and show your work)](#how-to-submit-this-lab-and-show-your-work)
- [Lab Notebook Questions](#lab-notebook-questions)
  
[Click here to access the lab procedure as a Jupyter Notebook](https://drive.google.com/file/d/1L9A7I6bFJiyEUfGXdtL4odLqkCO2ROKf/view?usp=sharing)

# Lecture and Live Coding

Throughout this lab, you will see a Panopto icon at the start of select sections.

This icon indicates there is lecture/live coding asynchronous content that accompanies this section of the lab. 

You can click the link in the figure caption to access these materials (ND users only).

Example:

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
  <td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=df2efb55-a837-454e-910d-ad820163cda5">Lab overview</a></td>
  </tr>
  </table>
  
<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
<td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?pid=266f95e7-65bd-4718-9a97-ae300135e32a">Lecture/live coding playlist</a></td>
  </tr>
  </table>

# Lab Notebook Template

Lab notebook template:
- [`.py` file](https://drive.google.com/file/d/1SzNANtFLxwt0trPVVYyLRBHzQJ6ixOUE/view?usp=sharing)
- [Jupyter Notebook](https://drive.google.com/file/d/1t5_e7qMH-filkLUpPkl2O4ae5UlzWT4p/view?usp=sharing)

# Dictionaries

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
  <td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5a24f407-5860-4d8b-8aea-ad8201622e0f">Dictionaries</a></td>
  </tr>
  </table>

<p align="center"><img src="https://github.com/kwaldenphd/python-dictionaries-sets/blob/main/figures/Dic_1.png?raw=true"></p>

<p align="center"><img src="https://github.com/kwaldenphd/python-dictionaries-sets/blob/main/figures/Dic_2.png?raw=true"></p>

1. A dictionary is a mapping between a set of indices (keys) and a set of values. 

2. Each key maps to a value. 

3.  The association of a key and a value is called a key-value pair.

## Creating a Dictionary

4. We have two options for creating a dictionary.

5. We can use the `dict()` function or the `{}` syntax.

6. Examples for each:

```Python
# creating empty dictionary using dict()
english_to_french = dict({})

# check variable type
type(english_to_french)

# create dictionary this time with key-value pairs
english_to_french = dict({
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
})
```

```Python
# create empty dictionary using curly brackets {}
english_to_french = {}

# check variable type
type(english_to_french)

# create dictionary this time with key-value pairs
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}
```

## Interacting With A Dictionary

7. Now that we have a dictionary, we can start to bring in some of the syntax covered in previous labs.

```Python
# show dictionary
print(english_to_french)
```

8. Notice that when we print the dictionary, the key-value pairs are **unsorted** and do not appear in the order in which we added them.

9. Due to the nature of the dictionary data structure, we cannot make any assumptions about the order in which items appear in the dictionary.

10. We can use the index operator to read the value for a particular key.

```Python
# access value for 'one' key
english_to_french['one']
```

11. If we try to access the value for a key that does not exist, Python will return a KeyError.

```Python
# code that will return a key error
english_to_french['asdf']
```

12. We can test for membership using  the `in` operator.

```Python
# check for 'asdf' string
'asdf' in english_to_french

# check for 'one' string
'one' in english_to_french

# check for 'un' string
'un' in english_to_french
```

13. Each of these commands returns a Boolean `True` or `False` value.

14. Notice the last command returned `False` because the `in` operator is looking at keys, not values in the dictionary.

15. We can use the `.keys()` method to get a list of all keys in the dictionary.

```Python
# output keys in dictionary
print(english_to_french.keys())
```

16. We can use the `.values()` method to get a list of all the values in the dictionary.

```Python
# output values in dictionary
print(english_to_french.values())
```

17. We can also add key-value pairs to our dictionary using the index operator and an assignment statement.

18. To see that in Python syntax:

```Python
# add key-values pairs to dictionary
english_to_french['six']   = 'six'
english_to_french['seven'] = 'sept'
english_to_french['eight'] = 'huit'
english_to_french['nine']  = 'neuf'
english_to_french['ten']   = 'dix'

# show updated dictionary
print(english_to_french)
```

19. The first part of each line of code creates a new key and assigns the value (the string to the right of the assignment operator, or equals sign) to that key, giving us a new key-value pair.

## Iteration and Dictionaries

20. The previous lab talked about the concept of "iteration," and we're going to see it at work here as well.

21. Say we wanted to iterate by keys through our dictionary.

22. We could use a `for` loop to tell Python "`FOR` each key-value pair in my dictionary...do this thing!"

23. An example that tells Python to print the key for each key-value pair.

```Python
# for loop that outputs keys
for key in english_to_french.keys():
  print(key)
```

24. We could modify the print statement nested in the for loop to output the key and value.

```Python
# for loop that outputs key-value pairs
for key in english_to_french.keys():
  print(key, english_to_french[key])
```

25. And, we wouldn't actually need to use the `.keys()` method when iterating by keys.

```Python
# alternate syntax for outputting key-value pairs
for key in english_to_french:
  print(key, english_to_french[key])
```

26. We can also iterate by key-value pairs, using the `.items()` method.

```Python
# for loop that outputs key-value pairs using items
for key, value, in english_to_french.items():
  print(key, value)
```

27. In this example, we told Python to look at the key and value in each key-value pair and print the pair.

## Dictionary Lab Notebook Question

Q1: Create a dictionary on a topic of your choosing. Include at least 7 key-value pairs.
<ol type="a">
 <li>Add new elements to your dictionary.</li>
 <li>Update an element in your dictionary.</li>
 <li>Print a list of all the keys in your dictionary.</li>
 <li>Print a list of all the values in your dictionary.</li>
 </ol>
 
# Sets

<table>
 <tr><td>
<img src="https://elearn.southampton.ac.uk/wp-content/blogs.dir/sites/64/2021/04/PanPan.png" alt="Panopto logo" width="50"/></td>
  <td><a href="https://notredame.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5a24f407-5860-4d8b-8aea-ad8201622e0f">Sets</a></td>
  </tr>
  </table>

28. A set is an unordered collection of unique objects. Sets are primarily used to see if an object or value is in the collection (membership).

<p align="center"><img src="https://github.com/kwaldenphd/python-dictionaries-sets/blob/main/figures/Sets.png?raw=true"></p>

29. There are many different types of set operations, but this lab is just going to focus on testing for membership.

30. That is, looking to see if a particular value is `in` a set.

31. HINT: We've seen `in` operators before...

## Creating Sets 

32. We can create the set using `set()`

```Python
# create empty set and assign to s variable
s = set()

# check s variable type
type(s)

# create set with values
s = set([0,1,2])

# show set values
s
```

## Testing for Membership

33. Now that we have a set with values, we can test for membership using the `in` operator.

```Python
# create set with values
s = set([0, 1, 2])

# test if 0 is in s
0 in s

# test if 7 is in s
7 in s
```

34. The last two lines of code return Boolean `True` or `False` statements.

## Adding and Removing Items 

35. We can add items to our set using `.add()`.

```Python
# create empty set
s = set()

# add values to set
s.add(0)
s.add(1)
s.add(2)

# show new set with values
s
```

36. We can also remove values from our set using `.remove()`.

```Python
# create set with values
s = set([0, 1, 2])

# remove 1 number value from set
s.remove(1)

# show updated set
s
```

## Set Lab Notebook Question

Q2: Create the set `s` with the following values: `[1, 3, 5, 7, 9]`
<ol type="a">
  <li>Test to see if the value <code>11</code> is a member of the set.</li>
  <li>Test to see if the value <code>7</code> is a member of the set.</li>
  <li>Add a value to the set.</li>
  <li>Remove a value from the set.</li>
 </ol>

# Additional Lab Notebook Questions

Q3: What is the difference between a `list` and a `dict`? When would we prefer one over the other?

Q4: What is the difference between a `dict` and a `set`? When would we prefer one over the other?

Q5: Include a link to your Replit project workspace.

# How to submit this lab (and show your work)

Moving forward, we'll submit lab notebooks as `.py` files. 

One option is to have a `.py` file that you use to run code and test programs while working through the lab. When ready to submit the lab notebook, you add comments and remove extraneous materials.

Another option is to have an "official" `.py` file that you are using as a lab notebook (separate from your working/testing file). Use comments in Python to note when you are starting a new question (as well as answering a question).
  * Example: `Lab5_Notebook_Walden.py`

What gets submitted as the lab notebook is the `Lab5_Notebook_Walden.py` file.
- When in doubt, use comments
- Be sure you are using comments to note what question you're responding to

# Lab Notebook Questions

Lab notebook template:
- [`.py` file](https://drive.google.com/file/d/1SzNANtFLxwt0trPVVYyLRBHzQJ6ixOUE/view?usp=sharing)
- [Jupyter Notebook](https://drive.google.com/file/d/1t5_e7qMH-filkLUpPkl2O4ae5UlzWT4p/view?usp=sharing)

Q1: Create a dictionary on a topic of your choosing. Include at least 7 key-value pairs.
<ol type="a">
 <li>Add new elements to your dictionary.</li>
 <li>Update an element in your dictionary.</li>
 <li>Print a list of all the keys in your dictionary.</li>
 <li>Print a list of all the values in your dictionary.</li>
 </ol>

Q2: Create the set `s` with the following values: `[1, 3, 5, 7, 9]`
<ol type="a">
  <li>Test to see if the value <code>11</code> is a member of the set.</li>
  <li>Test to see if the value <code>7</code> is a member of the set.</li>
  <li>Add a value to the set.</li>
  <li>Remove a value from the set.</li>
 </ol>
  
Q3: What is the difference between a `list` and a `dict`? When would we prefer one over the other?

Q4: What is the difference between a `dict` and a `set`? When would we prefer one over the other?

Q5: Include a link to your Replit project workspace.
