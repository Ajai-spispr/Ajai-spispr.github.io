---
layout: post
title:  "Python Guide part-one"
date:   2019-11-17 09:25:54 +0530
categories: blog programming python
---

# Python programming language

Python is a general-purpose object-oriented  programming language created by Guido Van Rossum. It is known for its
* Readable and Maintainable Code
* Friendliness to beginners
* Simplified software development
* Support to multiple programming paradigms like  

This guide is part one of my python programming guide series. The intened audience are the people who are already familiar with a programming language and quickly want to learn Python. This guide can be used as a quick refresher, as I tried to cover the essential Python features.

## Hello World

### *Hello world*
In Python we can print a string literal using print function. 
Python string values should be enclosed in a double or single quote.
~~~~
print("Hello World") # Hello World
print('Hello World') # Hello World
~~~~

## Expression and Statement

Expressions are something which evaluates to a value.
~~~~
# 10 + 3 is a expression as it evaluates to 13
10 + 3 #13 
~~~~

Statements are comprised of expressions and they do some action.
~~~~
x = 10 + 3 //This is a statement, because the expression is evaluated and assigned to variable x
~~~~

## Comments 
Comments in code help us in documentation and readability. In Python introducing '#' symbol makes all the statement towards its right non executable.
~~~~~
print('This is not a comment')
#print('This is a comment')
print("# This won't get commented")
~~~~~

## *Docstring*

Docstrings are Python's way of documenting the code. Which are ignored like comments.
Most of the Python dev tools render docstring as help text.

~~~~~
def checkForpalindrome(phrase):
    '''
    Checks if a phrase is a palindrome  

    parameters:
    phrase (string): phrase to check

    returns : 
    0 -> if the phrase is palindrome
    -1 -> if it is not 
    '''
    return phrase.find(phrase[::-1])
~~~~~

## Variables

Variable is a reserved memory location to store values.
Python is a dynamically typed language so a variable can hold a different type of value than the one it is initiated with.
Since it is an interpreted language, it won't know the type of a variable until the code is run.

~~~~
a = 100
print(a) #100
a = 'Dynamically typed'
print(a) # Dynamically typed
~~~~

## Datatypes

Data types represent the type of data stored in a Python variable. Everything in Python are objects, so we can say data type is nothing but the class name.

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

In Python, No value can be denoted by "None" object. This is similar to null in popular programming languages.
~~~~
no_value = None
type(no_value) #NoneType
~~~~

Python has many other data types as well, for example it even support complex numbers.
~~~~
c = 5 + 3j
type(c) #complex
print(c + 3) #8 + 3j
~~~~
## Operators 

Operators are symbols that programming languages use to carry out arithmetic and logical operations. 

Following are the most common Python operators.
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

~~~~
# Examples of logical operators
# Python uses 'and' and 'or' instead of && and ||

x = 4 
y = 7

if x == 4 and y == 7:
  print('python and statement')

if x == 5 or y ==7:
  print('python or statement')
~~~~

In Python we can even override the function of an operator, Which we will see in later blog posts.

## Truthy and Falsy values

Apart from the boolean values, 'True' and 'False', Python evaluates certain values to 'True' and 'False'.

Truthy and Falsy values are syntactic sugar in Python, which helps us write elegant code. We can figure out whether an expression evaluates to truth or false by using bool() function 

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

Flow control in Python helps us in making code control flow decisions.

*If...else statements*

The code in if block gets executed, if the expression evaluates to a truthy value. If not, the else block is executed.

~~~~
'''
if expression:
 Statement
else:
 Statement
'''
x = 10;
if x > 10 : 
    print('x is greater than 10')
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
    print('x is greater than 10')
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
   print('The count is ' + str(count))
   count = count + 1
~~~~

*For loop*

~~~~
for i in range(10):
    print('Hello')

for i in range(2, 20):
    print(i)
~~~~

Python doesn’t support do...while loops which most of the languages support.

## Functions

Function is a group of related statements which perform a specific task. They make our code modular and manageable.

Functions which don't have a return type are called procedures in Python.

*Without  return type*
~~~~
#function without parameter
def print_hello_world():
    print("Hello world")

#function with parameter
def function_without_return_value(param):
    ''' 
    functions that doesn’t have a return type are 
    called as procedures 
    '''
    print("param for this function is " + param)
~~~~
*With return type*
~~~~
def function_with_return_type(param):
    return param *2
~~~~
## Indentation

Python uses indentation to organize code blocks. A code block (body of a function, loop, if statement) starts with a indentation and ends with a first un-indented line. The amount of indentation for the code is up to you, but be consistent with your indentation, otherwise Python interpreter will give indentation error.

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
    print('Python hits two birds with a single stone')
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
