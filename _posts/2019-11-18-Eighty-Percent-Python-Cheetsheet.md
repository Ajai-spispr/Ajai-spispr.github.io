---
layout: post
title:  "Python Cheetsheet - Eighty Percent python you use"
date:   2019-11-18 15:25:54 +0530
categories: programming python
---

# Python programming language

Python is a general purpose object oriented programming language created by Guido Van Rossum. python is known for
* Readable and Maintainable Code
* It is friendly for beginners
* Simplifies software development
* Supports multiple programming paradigams



## Hello World

### *Hello world*
We can print a string literal using print function. 
python doesen't care about double or single quotes
~~~~
print("Hello World")
print('Hello World")
~~~~

## Expression and Statement
//todo

### *Print Hello World 10 times*

We can print Hellow World 10 times, using a loop 
~~~~
for i in range(10):
    print("Hello")
~~~~

*Alternate Way*

~~~~
print("Hello World\n"*10)
~~~~

## Comments 
Comments in code help us in documentation and readability. In python introducing '#' symbol makes all the statement towards its right non executable.
~~~~~
print("This is not a comment")
#print("This is a comment")
print("# Comment starts from here")
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
python is not statically typed language so a variable can hold a variable of different type than the one it is initiated with.

~~~~
a = 100
print(a) #100
a = 'statically typed'
print(a)
~~~~

## Datatypes

Data types represent the type of data stored in a python variable. Everything in python are objects, so we can say datatype is nothing but the class name.

Some of the most used data types are listed below.

*Integer type*
~~~~
int_type = 10
type(int_type)
~~~~
*Floating point*
~~~~
floting_type = 4.2
type(floating_type)
~~~~
*String*
~~~~
string_type ="All is well"
type(string_type)
~~~~
*Boolean type*
~~~~
bool_true = True #case sensitive 
type(bool_true)
bool_false = False #case sensitive 
type(bool_false)
~~~~

Python has lot other data types as well. some are complex like complex numbers.

## Operators 

Operators are symbols we programming languages use to carry out arithmetic and logical operations. 

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

print(add) 
print(sub) 
print(mul) 
print(div1) 
print(div2) 
print(mod) 
~~~~

In python we can even override the function of a operator.

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
~~~~

## Flow control

Flow control in python helps us in making code control flow decisions.

*If,else  condition*

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
        print("this is not a empty string")
    else:
        print("empty string")
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
    print("Hello")
~~~~

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
## functions

*Without  return type*
~~~~
def function_without_return_value(param):
    ''' 
    functions that dosen't have a return type can also be 
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
    print('python hits two birds with one stone')
    if love_for_python < 10:
        print('you are not cool')
    elif 10 < love_for_python < 50
        for i in range(5):
            print('Thank you!')
    if love_for_python > 50
        for i in range(love_for_python):
            for i in range(2):
                print('Python love you twice more than that')

~~~~
## Python String

Some common string operations
In python string's are immutable
*Slicing string*
~~~~
var1 = "Python is awesome"
print("var1[0]:",var1[0])
print("var1[1:5]:",var1[1:5])
~~~~
*contains*
~~~~
var1 = 'Guido van Rossum'
print('van' in var1)
print('Gandhi' not in var1)
~~~~
*other major string functions*
~~~~
fact = 'java is older than python'
fact.replace('older', 'younger')
print(":".join("Python"))	
print(''.join(reversed(string)))
print(word.split(' '))
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
