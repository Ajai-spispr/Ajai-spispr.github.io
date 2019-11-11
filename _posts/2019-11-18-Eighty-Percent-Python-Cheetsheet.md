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
def function_with_return_type(param):
    return param *2
## Intendation
//todo

## Python String

Some common string operations

~~~~
var1 = "python is awesome"
var2 = "does it bites"
print ("var1[0]:",var1[0])
print ("var2[1:5]:",var2[1:5])
~~~~

//todo
https://www.guru99.com/learning-python-strings-replace-join-split-reverse.html

## list
//Todo

## dictionary
//Todo

## tuples
//todo

## Set
//todo

## python modules

//Todo continue and pass statements