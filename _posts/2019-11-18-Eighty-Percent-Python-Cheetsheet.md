---
layout: post
title:  "Python Cheetsheet - Eighty Percent python you use"
date:   2019-11-18 15:25:54 +0530
categories: programming python
---


## Hello World

### *Hello world*
Print a literal string on standard output
python doesen't care about double or single quotes
~~~~
print("Hello World")
print('Hello World")
~~~~

### *Print Hello World 10 times*

Loop to execute some code a constant number of times

~~~~
for i in range(10):
    print("Hello")
~~~~

*Alternate Way*

~~~~
print("Hello World\n"*10)
~~~~

## Comments 

~~~~~
print("This is not a comment")
#print("This is a comment")
~~~~~

## *Docstring*

Docstrings are python way of documenting the code. They are also ignored by the python like comments/

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

Variable is a reserved memory locataion to store values
python is not statically typed language so a variable can hold a variable of different type than the one it is initiated with

~~~~
a = 100
print(a) #100
a = 'statically typed'
print(a)
~~~~

## Datatypes

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
Python has other data complex data types like complex numbers.

## Operators 

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

## Flow control

*If,else  condition*

~~~~
'''
if expression
 Statement
else 
 Statement
'''
x = 10;
if x > 10 : 
    print('x is greater than 10)
else : 
    print('x is lesser than 10')
~~~~

*elif*

~~~~
x = 10;
if x > 10 : 
    print('x is greater than 10)
elif x == 10:
    print('x is equal to 10')
else : 
    print('x is lesser than 10')
~~~~

## Loops - different types

While loop

~~~~
count = 0
while (count < 9):
   print('The count is ' + count)
   count = count + 1
~~~~

## do while loop

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
    print('one stone two mango philosophy')
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
normal_set = set(["a", "b","c"]) 
~~~~

## Iterating python collections


## python modules

//Todo continue and pass statements


## Exercises

* How to do all common set operations using python

