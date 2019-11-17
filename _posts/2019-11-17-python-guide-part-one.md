---
layout: post
title:  "Python guide part-one"
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
In python we can print a string literal using print function. 
python string values should be enclosed by a double or single quote.
~~~~
print("Hello World") # Hello World
print('Hello World") # Hello World
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
Python is a dynamically typed language so a variable can hold a variable of different type than the one it is initiated with.
Since it is a interpreted language, it won't know the type of a variable until the code is run.

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

Truthy and falsy values are syntactic sugar in python, which helps us write elegant code. We can figure out whether a code expression evaluates to truth or false by using bool() function 

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

Python doesn’t supports do while loops which most of the languages support.

## functions

Function is a group of related statements, which perform a specific task. Functions make our code modular and manageable.
Functions which don't have a return type are called procedures in python.

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
## indentation

Python uses indentation to organize code blocks. A code block (body of a function, loop, if statement) starts with a indentation and ends with a first unintended line. The amount of indentation for the code is up to you. But be consistent with your indentation, otherwise python interpreter will give indentation error.

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