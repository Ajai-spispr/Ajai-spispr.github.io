---
layout: post
title:  "Python guide series Two"
date:   2020-01-11 15:25:54 +0530
categories: blog programming python
---

# Python Guide - part 2

This is part 2 of the python guide series please go through part one first, If you are new to this sereis.

## Python String

Some common string operations

*Slicing string*
In python strings are indexed with respect to each character starting from 0. In the string "Python.", character at index 0 is "P" and character at index 6 is ".".
The syntax for slicing string is. 
`[Start index (included): end index (excluded)]`

~~~~
var1 = "Python is awesome"
print("var1[0]:",var1[0]) 
print("var1[1:5]:",var1[1:5])
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
print(word.index("world"))
fact = 'java is older than python'
fact.replace('older', 'younger')
print(":".join("Python"))	
print(word.split(' '))
~~~~

*Triple quote string*
If we want to use string which spans multiple line, use triple quote.
~~~~
triple_quote = """Multiple line string can be created using triple quotes. Triple quotes allows to have "double-quoted" string and 'single-quoted' string in a string."""
~~~~

## Data structures and collections

Collections in python are objects that store data. These objects are implementations of various data structures. For a beginner no need to stress on the internal data structures.

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

## tuples

*common tuple operations*

~~~~
# creating a empty tuple
my_tuple0 = ()
# creating a tuple with data
my_tuple = (1, 2, 3, 4, 5)
# typles can also hold different type of data
my_tuple[0:3]
another_tuple = tuple()
abc = tuple([1, 2, 3])
abc_list = list(abc)
~~~~
## dictionary

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

## Set
*Common set operations*

~~~~
thisset = {"apple", "banana", "cherry"}
normal_set = set(["a", "b","c"]) 
"banana" in thisset
~~~~

## Choosing the right data structure

//to do

## Iterating python collections

~~~~
for <var> in <iterable>:
    <statement(s)>
~~~~

*iterating overa a list*

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