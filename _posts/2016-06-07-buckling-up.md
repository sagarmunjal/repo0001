---
layout: post
title: Buckling Up!
date: '2016-06-07 01:51:19 +0530'
categories: javascript basics
published: true
---

### 1.1 Setting up the environment

### 1.2 Getting to know language

### 1.3 Program Structure


---

---

---

#### **1.1 Setting up the environment:** 

Google chrome and your workstation. Yes, that’s pretty much all.
We will really set up a proper environment where javascript runs how it gets compiled in a separate post. I would call it a proper environment with some HTML, etc. The google chrome JS console.

---

#### **1.2 Getting to know the language**

1. Syntax
2. Values


##### 1. Syntax

There are few characters I would want you to see as follows, as they are widely used in JS.

- Javascript comments : 

They are an awesome way to increase user readability of your code.
JavaScript ignores any statement which starts with “ // “ and the end of the line.

Ex :

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="1-2"></code>


- Multiline Javascript comments : 

Similarly, We can have multiline comments in JavaScript also in which javascript ignore anything between /*  */

Ex :

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="4-8"></code>

- Semicolons are optional but should not always be ignored:

We write commands in a programming language, these commands are small instructions which are given to the computer called statements. Each statement ends with a semicolon however semicolons are optional after some statements.
 
Ex : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="10-13"></code>

  
- Missing semicolon pitfall related to long sentences:

Let’s declare a long variable.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="15-19"></code>
 
This would definitely give out an error because JS compiler treats the above as follows:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="21-24" data-gist-highlight-line="21"></code>
 

- How to evade this error using backslash ( \ )
 
Backslash operator helps us to evade the error by telling the console to ignore the new line.
 
Defining words with single quotes (Another pitfall for beginners ) :
 
Lets define a string:
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="26-27"></code>
 
The above example gives an error because the execution stops after the second single quote at ‘how’
 
- To avoid this error we can simply use the backslash.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="26,29-30"></code>

##### 2. Values 

---
### **1.3 Program Structure: ** 
1. Environment
2. Express and Statements
3. Variables

#### 1.3.1 Environment :  

JS environment comprises of what we program also what we do not program i.e. default. Every set of instruction when together runs in the JavaScript engine is a part of the JS environment. 
This environment comprises of default and user inputted set of instructions.

#### 1.3.2 Expressions and statements:
An expression is as small as simply typing a value followed by a semicolon ( ; ) 
For ex : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="33-34"></code>

But as any languages consists of sub-sentences which combine to make complete sentences, similarly in JS to convey something, we can have a set of expressions which can be complex or simple. 

*To explain fully, if an expression corresponds to sentence fragment, then a statement corresponds to full sentences. *

#### 1.3.3 Variables:
 
Variables are a way of assigning values, its something we do in our daily lives to make our work simpler. They are simply used to name something so you do not forget.

Now just imagine would it not be weird that everytime if Josh who has curly hair, black eyes, pink lips and short legs would be called as “ I introduce you to the one with the curly hair, black eyes, pink lips and short legs”. Would that really make sense? Would it not be simply easier to say “ i introduce you to Josh”.
 
That’s why we simply create variables. To remember and to make our lives simpler.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="36-40"></code>
 
- Rightful and wrongful declaration:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="44-47"></code>

 
- JS is case sensitive:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="49-51"></code>
 
- These are two different variables.
 
There are words which we can’t use while defining variables because they already exist in the JS environment. 
 
Var, function, return, class, implements



#### 1.3.4 User Interaction:  
a. Alert
b. Console.log
c. Prompt
d. Confirm
e. Comments

 
a. Alert: 

A new small dialog bogs appears on your screen alerting whatever message you alert in the parenthesis. Check out the syntax below and try yourself.
 
Syntax: 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="53-54"></code>
 
b. Console.log: 

This is pretty much works in a similar way, difference it it logs the message in the console that we use to define and declare our JS types etc.
 
Syntax:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="56-57"></code>
 
c. Prompt: 

Prompt allows to ask user to take values from the user input. This is very important to define customized variables.
Prompt asks for two arguments, one, which is the text and the default, which is optional argument, stores the default value in the variable.
 
Syntax:
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="59-62"></code>


d. Confirm:  

It is similar to prompt but instead of a value it stores boolean value in the variable corresponding to the “OK” and “cancel” the user is prompted with. See the following example to understand better.
 
Syntax : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="64-65"></code>






