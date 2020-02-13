---
layout: post
title:  "Python guide part two"
date:   2020-02-11 15:25:54 +0530
categories: blog programming python
---



This is part 2 of the python guide series please go through [first part](http://www.ajraj.me/blog/programming/python/2019/11/17/python-guide-part-one.html), If you are new to this series.

## Python string

Strings are the most important and widely used data type in any programming language. Strings can be visualized as an array of characters.

## Common string operations

*Slicing strings*

In python, strings are indexed with respect to each character starting from 0. In the string "Python", character at index 0 is "P" and character at index 5 is 'n'.
The syntax for slicing string is. 

`[Start index (included): end index (excluded)]`

~~~~
str = "Python is awesome"
print("str[0]:",str[0]) 
print("str[1:5]:",str[1:5])
~~~~

*Advanced slicing*

Python index can be in negetive numbers also. It indexes string in reverse direction starting with -1, as shown in below chart.

|__0__|__1__|__2__|__3__|__4__|__5__|__6__|__7__|__8__|__9__|__10__|__11__|__12__|__13__|__14__|__15__|__16__|__17__|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|p|r|o|g|r|a|m|m|i|n|g| |i|s| |f|u|n|
|__-18__|__-17__|__-16__|__-15__|__-14__|__-13__|__-12__|__-11__|__-10__|__-9__|__-8__|__-7__|__-6__|__-5__|__-4__|__-3__|__-2__|__-1__|

~~~~
txt = "programming is fun"
print(txt[-18])
print(txt[-1])
~~~~

*contains*
~~~~
var1 = 'Guido van Rossum'
print('van' in var1)
print('Gandhi' not in var1)
print('Gandhi' in var1)
~~~~
*other major string functions*
~~~~
str = "Hello world"
# To find the index of a string in another string
print(str.index("world"))
# Replacing one string with another
fact = 'java is older than python'
fact = fact.replace('older', 'younger')
print(fact)
#Spliting a string	
print(str.split(' '))
~~~~

*Triple quote string*

If you want to use a string which spans multiple lines, use triple quote to represent it.
~~~~
triple_quote = """Multiple line string can be created using triple quotes. Triple quotes allows to have "double-quoted" string and 'single-quoted' sub strings within in a string."""
~~~~

## Data structures and collections

Collections in python are objects that store data. These objects are implementations of various data structures. The internals of these data structures  are complex and interesting, but as a begineer we can use them without knowing the details.
Before learning about collections we need to understand immutability.

## Immutability
Everything in python is an object which can be either mutable or immutable.
Mutable objects can be modified after creation, immutable objects can't be modified.

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



## List

A list data structure is used to store ordered sequence of heterogeneous elements. It is mutable and used to store data dynamically.

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
# sorting a list
alpha_list = [34, 23, 67, 100, 88, 2]
alpha_list.sort()
# slicing a list
alpha_list[0:3]
~~~~

*When to use a list*
* Python doesn't support arrays natively, so whenever you need an array use a list
* When you want a flexible data structure to store data, you can insert, delete, update in any index 
* When you want to store hetrogeneous data
* When you want to store duplicate values

## Tuples

Tuples is an immutable data structure used to store sequence of hetrogenous elements. Once they are created, they cannot be modified.

*common tuple operations*

~~~~
# creating a empty tuple
my_tuple0 = ()
# creating a tuple with data
my_tuple = (1, 2, 3, 4, 5)
# typles can also hold different type of data
my_tuple1 = (1, 2, '3', '', 5)
#slicing a tuple
my_tuple1[0:3]
# converting a list to tuple
abc = tuple([1, 2, 3])
# converting a tuple to list
abc_list = list(abc)
~~~~

*Tuples vs list*
* Tuples have fixed size, whereas lists are dynamic
* Tuples don't have methods to append or modify and remove elements
* We can still find an element in tuple as this process dosen't change the object's state
* Tuples are faster than lists as they are optimised internally for searching and iteration
* Tuples can be used safely in multi-threaded application without data loss

*When to use a tuple*
* When you want to store a sequence of data which dosen't change
* Tuples can be used as dictionary keys  (Which we will see below)
* When you need to search through a sequence faster

## Dictionary

Dictionaries in python are an unordered collection of keys and values.

*Common dictionary operations*
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
* When you need a key-value data storage
* Dictionary enables a convenient way to search for values
* Retriving and modifying values are blazingly fast

## Set

A set is an unordered collection of data that is iterable, mutable and has no duplicate elements.

*Common set operations*

~~~~
thisset = {"apple", "banana", "cherry"}
normal_set = set(["a", "b","c"]) 
"banana" in thisset
~~~~

*list vs set*
* Set requires items to be hashable, list doesn't
* Set forbids duplicates, list doesn't

*When to use a set*
* To store unique values


## Some cool slicing 

The syntax for slicing operater is `itr[start:end:step]`
~~~~
# without step argument
"1234"[0:2] # will return "12"
# with step argument
"12345678"[0:6:2] #[1,3,5,7] every 2nd number from 0 and 6
#usage of start,end and step values are optional
#without end and step
"1234"[1:] # "234"
"1234"[:3] # "123"
"1234"[1:3] # "23"
"1234"[1:3:] # "23"
"1234"[::2] # "13"
"1234"[::] # "1234"
"1234"[:] #"1234"
#negative step argument can reverse the sequence
"1234"[::-1] "4321"
#slicing can also be used to replace multiple items
lis = [0, 1, 2, 3]
lis[::2] = ['zero', 'Two']
# we can also delete a part of list
lis = [0, 1, 2, 3]
del lis[::2]
~~~~

## Iterating python collections

~~~~
for <var> in <iterable>:
    <statement(s)>
~~~~

*Iterating over a list*

~~~~
# different ways of iterating over a list
list = [1, 3, 5, 7, 9]
for i in list:
    print(i)

# If you want the index of elements in the loop
length = len(list)
for i in range(length): 
    print('index is ' + str(i)) 
    print('value is ' + str(list[i]))

# while loop
while i < length: 
    print(list[i]) 
    i += 1
# list comprehensions (More about this in future posts)
li = [print(i) for i in list] 

# one another way of getting index and values in list
for i, val in enumerate(list): 
    print (i, ",",val) 
~~~~

*Iterating over a tuple*

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
a_dict = {"one":1, "two":2, "three":3}
# looping the keys
for key in a_dict:
    print(key, ' ', a_dict[key])

# looping the values
for item in a_dict.items():
    print(item)

# looping key and values
for key, value in a_dict.items():
    print(key, '::', value)

~~~~

