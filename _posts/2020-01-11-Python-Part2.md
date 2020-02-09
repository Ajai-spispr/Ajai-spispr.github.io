---
layout: post
title:  "Python guide series Two"
date:   2020-01-11 15:25:54 +0530
categories: blog programming python
---

# Python Guide - part 2

This is part 2 of the python guide series please go through first part, If you are new to this series.

## Python String

Strings are the most important and widely used data type in any programming language. Strings can be visualized as a array of characters.

## Common string operations

*Slicing strings*

In python strings are indexed with respect to each character starting from 0. In the string "Python.", character at index 0 is "P" and character at index 6 is ".".
The syntax for slicing string is. 
`[Start index (included): end index (excluded)]`

~~~~
str = "Python is awesome"
print("str[0]:",str[0]) 
print("str[1:5]:",str[1:5])
~~~~

*Advanced slicing*

Python index string in reverse direction also starting with -1, as shown in below chart.

|__0__|__1__|__2__|__3__|__4__|__5__|__6__|__7__|__8__|__9__|__10__|__11__|__12__|__13__|__14__|__15__|__16__|__17__|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|p|r|o|g|r|a|m|m|i|n|g| |i|s| |f|u|n|
|__-18__|__-17__|__-16__|__-15__|__-14__|__-13__|__-12__|__-11__|__-10__|__-9__|__-8__|__-7__|__-6__|__-5__|__-4__|__-3__|__-2__|__-1__|

~~~~
word = "programming is fun"
print(word[-18])
print(word[-1])
~~~~

*contains*
~~~~
var1 = 'Guido van Rossum'
print('van' in var1)
print('Gandhi' not in var1)
~~~~
*other major string functions*
~~~~
word = "Hello world"
# To find the index of a string in another string
word.index("world")
# Replacing one string with another
fact = 'java is older than python'
fact.replace('older', 'younger')
#Spliting a string	
print(word.split(' '))
~~~~

*Triple quote string*
If you want to use string which spans multiple line, use triple quote to reprasent that.
~~~~
triple_quote = """Multiple line string can be created using triple quotes. Triple quotes allows to have "double-quoted" string and 'single-quoted' string in a string."""
~~~~

## Data structures and collections

Collections in python are objects that store data. These objects are implementations of various data structures. The internals of this data structures  are complex and interesting, but as a begineer we can use  them without knowing the details.
Before learning about collections we need to understand immutability.

## immutability
Everything in python is a object, objects can be either mutable or immutable.
mutable objects can be modified after creation, immutable objects can't be modified.

Object type | Description | Immutable?
--- | --- | ---
bool | boolean value | Yes
int | integer value | yes
float | floating -point number | yes
list | sequence of objects | no
tuple | sequence of objects | yes
str | character string | no
set | unordered set of distinct objects | yes
dict | key value pair map | no



## list

A  list datastructure is used to store ordered squence of hetrogeneous elements. It is mutable, and used to store data dynamically.

*creation*

Various ways of creating lists
~~~~
# creating empty lists
my_list = []
my_list = list()
# creating lists with data
my_list = [1, 2, 3]
my_list2 = ["a", "b", "c"]
# lists can hold different type of data
my_list3 = ["a", 1, "Python", 5]
# they can be nested too, 
my_nested_list = [[1, 2, 3], ['a', 'b', 'c']]
~~~~

*common list operations*

~~~~
my_list = [1, 2, 3]
my_list2 = ["a", "b", "c"]
# merging two lists
combo_list = my_list + my_list2
alpha_list = [34, 23, 67, 100, 88, 2]
# sorting a list
sorted_list = alpha_list.sort()
# slicing a list
alpha_list[0:3]
~~~~

*When to use a list*
* Python don't support arrays natively, so whenever you need an array
* When you want a flexible datastructue to store data, you can insert, delete, update in any index 
* When you want to store hetrogeneous data
* when you want to store duplicate values.

## tuples

Tuples  is a immutable datastructure used to store sequence of hetrogenous elements. Once they are created they cannot be modified.

*common tuple operations*

~~~~
# creating a empty tuple
my_tuple0 = ()
# creating a tuple with data
my_tuple = (1, 2, 3, 4, 5)
# typles can also hold different type of data
my_tuple1 = (1, 2, '3', '', 5)
#slicing a tuple
my_tuple[0:3]
another_tuple = tuple()
abc = tuple([1, 2, 3])
abc_list = list(abc)
~~~~

*tuples vs list*
* tuples have fixed size, whereas lists are dynamic
* tuples don't have methods to append or modify elements
* tuples don't have methods to remove elements
* we can still find a element in tuple as, it dosent change the objects state.
* tuples are faster than list, they are optimised internall for searching and iteration.
* tuples can be used safely in multi threaded application without data loss, using lists here with care.

*When to use a tuple*
* When you want to store a sequence of data which dosent change.
* tuples can be used as dictionary keys(Which we will see below).
* you need to search through a sequence faster.

## dictionary

Dictionaries in python is a unordered collection of key and values.

*common dictionary operations*
~~~~
my_dict = {}
another_dict = dict()
my_other_dict = {"one":1, "two":2, "three":3}
my_other_dict["one"]
my_dict = {"name":"Mike", "address":"123 Happy Way"}
my_dict["name"]
"name" in my_dict
my_dict.keys()
~~~~

*When to use a dictionary*
* dict associates with each key a value, which enables a convenient way to search for values.
* retriving values and modifying values are blazingly fast.

## Set

A Set is an unordered collection data type that is iterable, mutable and has no duplicate elements.

*Common set operations*

~~~~
thisset = {"apple", "banana", "cherry"}
normal_set = set(["a", "b","c"]) 
"banana" in thisset
~~~~

*list vs set*
* set requires items to be hashable, list doesn't.
* set forbids duplicates, list does not.

*When to use a set*
* To store unique values.

## TypeError: unhashable type
// to do 

## Some cool slicing 
// to do 

## Iterating python collections

~~~~
for <var> in <iterable>:
    <statement(s)>
~~~~

*iterating over a list*

~~~~
list = [1, 3, 5, 7, 9]
for i in list:
    print(i)

for i in range(length): 
    print(list[i]) 

while i < length: 
    print(list[i]) 
    i += 1

[print(i) for i in list] 

for i, val in enumerate(list): 
    print (i, ",",val) 
~~~~

*iterating over a tuple*

~~~~
T = (10,20,30,40,50)
for var in T:
    print (T.index(var),var)
~~~~
*Iterating over a set*
~~~~
s = {1,2,3,4}
for var in s:
    print(var)
~~~~

*Iterating over  a map*
~~~~
for key in a_dict:
    print(key, '->', a_dict[key])
for item in a_dict.items():
    print(item)
for key, value in a_dict.items():
    print(key, '->', value)
for key in a_dict.keys():
    print(key)
for value in a_dict.values():
    print(value)
~~~~
//Todo iterating a map
//iterating a tuple and a set

## Exception Handling

// todo

## python modules

//Todo continue and pass statements

~~~~
def hello_world():
    print("hello world")

def add(a,b):
    print(str(a+b))

hello_world()
~~~~

## Hangman game

//todo

## Exercises

* How to do all common set operations using python

## Todo

* Str() function    
* __ functions in python
* python passing * with parameters
* difference between enumerate, range and list
* Duck typing
* Different ways of printing in python
* is it is pass by memory or reference
* type casting
* __init why we need
* reading from keyboard
* srting - operations
* operator overriding in python
* python yield keyword
* floor and ceiling in float
* python variable scope

*Do while loop*

Python dosen't support do while loops but we can achieve them using below ways

~~~~
while True:
  stuff()
  if fail_condition:
    break
~~~~

or

~~~~
stuff()
while not fail_condition:
  stuff()
~~~~