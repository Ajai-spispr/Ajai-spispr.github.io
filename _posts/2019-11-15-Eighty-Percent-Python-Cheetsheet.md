---
layout: post
title:  "Python guide series one"
date:   2019-11-15 15:25:54 +0530
categories: blog programming python
---

# Python programming language

Python is a general purpose object oriented programming language created by Guido Van Rossum. It is known for its
* Readable and Maintainable Code
* Friendliness to beginners
* Simplified software development
* Support to multiple programming paradigams like 

This guide is part one of my python programming guide series. The intened audience are the people who are already familiar with a programming language and quickly want to learn Python. This guide can also used as a quick refresher, as I tried to cover the essential Python features.

## Hello World

### *Hello world*
In python we can print a string literal using print function. 
python string values should be enclosed by a double or single quote.
~~~~
print("Hello World") # Hello World
print('Hello World") # Hello World
~~~~

## Expression and Statement

Expressions are something which evalutes to a value.
~~~~
# 10 + 3 is a expression as it evaluates to 13
10 + 3 #13 
~~~~

Statements are comprised of expressions and they do some action.
~~~~
x = 10 + 3 //This is a statement, beacuse the expression is evaluated and assigned to variable x
~~~~

## Comments 
Comments in code help us in documentation and readability. In python introducing '#' symbol makes all the statement towards its right non executable.
~~~~~
print('This is not a comment')
#print('This is a comment')
print'"# This won't get commented')
~~~~~

## *Docstring*

Docstrings are python way of documenting the code. They are also ignored by the python like comments.
Most of python dev tools render docstring as help text.

~~~~~
def checkForPalliandrome(phrase):
    '''
    Checks if a phrase is a palliandrome 

    parameters:
    phrase (string): phrase to check

    returns : 
    0 -> if the phrase is palliandrome
    -1 -> if it is not 
    '''
    return phrase.find(phrase[::-1])
~~~~~

## Variables

Variable is a reserved memory locataion to store values.
Python is a dynamically typed language so a variable can hold a variable of different type than the one it is initiated with.
Since it is a interpreted language, it won't know the type of a variable untill the code is run.

~~~~
a = 100
print(a) #100
a = 'Dynamically typed'
print(a) # Dynamically typed
~~~~

## Datatypes

Data types represent the type of data stored in a python variable. Everything in python are objects, so we can say datatype is nothing but the class name.

Some of the most common data types are listed below.

*Integer type*
~~~~
int_type = 10
type(int_type) #int
~~~~
*Floating point*
~~~~
floting_type = 4.2
type(floating_type) #float
~~~~
*String*
~~~~
string_type ="All is well"
type(string_type) #str
~~~~
*Boolean type*
~~~~
bool_true = True #case sensitive 
type(bool_true) #bool
bool_false = False #case sensitive 
type(bool_false) #bool
~~~~
*No Value*
In python no value can be denoted by 'None" object. This is similar to null in popular programming languages.
~~~~
no_value = None
type(no_value) #NoneType
~~~~

Python has lot other data types as well. some are little complex like complex numbers.
~~~~
c = 5 + 3j
type(c) #complex
print(c + 3) #8 + 3j
~~~~
## Operators 

Operators are symbols programming languages use to carry out arithmetic and logical operations. 

Following are the most common python operators.
~~~~
# Examples of Arithmetic Operator 
a = 9
b = 4
  
# Addition of numbers 
add = a + b 
# Subtraction of numbers  
sub = a - b 
# Multiplication of number  
mul = a * b 
# Division(float) of number  
div1 = a / b 
# Division(floor) of number  
div2 = a // b 
# Modulo of both number 
mod = a % b 

print(add)  #13
print(sub)  #5
print(mul)  #36
print(div1) #2.25
print(div2) #2
print(mod)  #1
~~~~

In python we can even override the function of a operator. we will see that in later blog posts.

## Truthy and falsy values

Apart form boolean values 'True' and 'False', python evaluates certain values as 'True' and 'False'.

Truthy and falsy values are syntactic sugar in python, which helps us write elegant code. We can figure out wheather a code expression evaluates to truth or false by using bool() function 

~~~~
bool('ajai')#True
bool('') #False
bool('False') #True
bool(-1)#True
bool(0) #False
bool(193849) #True
bool(None) #False
~~~~

## Flow control

Flow control in python helps us in making code control flow decisions.

*If,else statements*

If statement takes a expression if the expression evaluates to a truthy value, if block is executed, otherwise else block is executed.

~~~~
'''
if expression:
 Statement
else:
 Statement
'''
x = 10;
if x > 10 : 
    print('x is greater than 10)
else : 
    print('x is lesser than 10')

def not_a_good_way_2_check_empty_string(param):
    '''
    This function check if the passed param is empty string or not
    '''
    if param:
        print('this is not a empty string')
    else:
        print('empty string')
~~~~

*elif*

For checking multiple expressions, we can use elif statement in python.
~~~~
x = 10;
if x > 10 : 
    print('x is greater than 10)
elif x == 10:
    print('x is equal to 10')
else : 
    print('x is lesser than 10')
~~~~

## Loops

Python supports while and for loops.

*While loop*

~~~~
count = 0
while (count < 9):
   print('The count is ' + count)
   count = count + 1
~~~~

*For loop*

~~~~
for i in range(10):
    print('Hello')

for i in range(2, 20):
    print(i)
~~~~

Python dosen't supports do while loops which most of the languages support.

## functions

Function is a group of related statements, which perform a specific task. Functions make our code modular and managable.
Functions which don't have a return type are called procedures in python.

*Without  return type*
~~~~
#function without parameter
def print_hello_world():
    print("Hello world")

#function with parameter
def function_without_return_value(param):
    ''' 
    functions that dosen't have a return type are 
    called as procedures 
    '''
    print("param for this function is " + param)
~~~~
*With return type*
~~~~
def function_with_return_type(param):
    return param *2
~~~~
## Intendation

Python uses intendation to to organize code blocks. A code block (body of a function, loop, if statement) starts with a intendation and ends with a first unintended line. The amount of intendation for the code is upto you. But be consistent with your intendation, otherwise python interpretor will give intendation error.

~~~~
block
    block 2
    statement in block 2
        block3
            block 4
        statement in block 3
~~~~
*In other languages*

~~~~
function {
    if block{

    }else if block{

    }else{
        loop{

        }
    }
}
~~~~

*In python*
~~~~
def fn_2_demonstarte_intendation(love_for_python):
    print('python hits two birds with a single stone')
    if love_for_python < 10:
        print('you are not cool')
    elif 10 < love_for_python < 50:
        for i in range(5):
            print('Thank you!')
    if love_for_python > 50:
        for i in range(love_for_python):
            for i in range(2):
                print('you are cool')

~~~~
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
Can be created by two ways
~~~~
my_list = []
my_list = list()
my_list = [1, 2, 3]
my_list2 = ["a", "b", "c"]
my_list3 = ["a", 1, "Python", 5]
my_nested_list = [[1, 2, 3], ['a', 'b', 'c']]
~~~~

*common list operations*

~~~~
my_list = [1, 2, 3]
my_list2 = ["a", "b", "c"]
combo_list = my_list + my_list2
alpha_list = [34, 23, 67, 100, 88, 2]
sorted_list = alpha_list.sort()
alpha_list[0:3]
~~~~

## tuples

*common tuple operations*

~~~~
my_tuple = (1, 2, 3, 4, 5)
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


## python modules

//Todo continue and pass statements

~~~~
def hello_world():
    print("hello world")

def add(a,b):
    print(str(a+b))

hello_world()
~~~~

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