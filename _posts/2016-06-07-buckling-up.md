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


### 1. Syntax

There are few characters I would want you to see as follows, as they are widely used in JS.

```
[] square brackets 
() parenthesis
; semicolon
'' single quotes
"" double quotes 
, comma separator
```


> - **Inline comment or Single line comments :** 

As you will make progress and become a Javascript ninja, you will understand the power of Source Code Styling. The trait of writing understandable and user friendly code comes with practice and attention to the details. 

Writing comments is just one of the many things that sets apart a good programmer and just a run-of-the-mill-programmer. Below we will see few examples of how to write comments.

They are an awesome way to increase user readability of your code.
JavaScript ignores any statement which starts with “ // “ and the end of the line.

Ex :

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="1-2"></code>


> - **Comment Block or Multiline comments :** 

Similarly, We can have multiline comments in JavaScript also in which javascript ignore anything between /*  */

Ex :

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="4-8"></code>

> - **Semicolons: When and when not to use**

Semicolons simply end a Javascript statement. 

We write commands in a programming language, these commands are small instructions which are given to the computer called **_statements_**. Each statement ends with a semicolon however semicolons are optional after some statements.

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="71-78"></code>

Semicolons are a part of JavaScript syntax language but we will help you where they must not be **LEFT OUT**. 

A small cheat sheet for THREE CASES when semicolons are 

(i)   Required 

(ii)  Optional

(iii) Avoid a semicolon 

(i)   Required 

Semicolons are REQUIRED when two statements are in the same line. 

Ex : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="12-14"></code>

(ii)  Optional

Semicolon is required to end statements but are optional if a statement is followed by a line break. 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="10-11"></code>

(iii) Avoid a semicolon 

- After a closing curly bracket of an if, for, while loop and a function body. See the example below to get the drift of it. 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="80-91"></code>

- After the round bracket of an if, for, while or switch statement

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="92-100"></code>


> - Missing semicolon pitfall related to paragraph with multiple lines:

Let’s declare a paragraph including multiple lines.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="15-19"></code>
 
There is a small bug in the statement. When the first sentence ends with a line break, JS compiler puts a semicolon after it and treats it as a separate _statement_. See the demonstration below how javascript compiler puts a semicolon at the line break. 
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="21-24" data-gist-highlight-line="21"></code>
 

> - **When to use backslash ( \ )**


 
Backslash tells the JS compiler to ignore the linebreak, a single quote and a double quote if in case we want these to be intentionally ignored.

Backslash is a very powerful tool and its very simple to understand. We can simply talk about the above example and few other more examples to dodge the error using a backslash. Let's walk through few small bugs below.  

_Practice yourself :_ 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="111-117"></code>


 
- BUG FIX ( LONG SENTENCE ) : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="101-108" data-gist-highlight-line="21"></code>

- BUG FIX ( when using words having single quotes like HOW'S, STEPHEN'S, etc )  :
 
Lets define a string having a word having a single quote:

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="26-27"></code>
 
The above example gives an error because the execution stops after the second single quote at ‘how’. We can fix this bug by simply prefixing the single quote by a backslash as shown below. 
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="26,29-30"></code>


### 2. Values 

We know what makes up the computer level. What human cell is to human body or what atom is to any physical matter, similarly, bits are to a computer program. 

So we can imagine computer programs as a vast big pool of bits. Refer to this [link](http://computer.howstuffworks.com/bytes.htm) to learn more about bits and bytes which make up the values. These bits come together and make a group to denote a certain value which are stored in some form in computers memory. How to manipulate these values in order to get the desired result is what depends on the developers. 



---

#### **1.3 Program Structure:**
1. Environment
2. Expressions and Statements
3. Variables

### 1. Environment :  

JS environment comprises of what we program also what we do not program i.e. default. Every set of instruction when together runs in the JavaScript engine is a part of the JS environment. 
This environment comprises of default and user inputted set of instructions.

### 2. Expressions and statements:
An expression is as small as simply typing a value followed by a semicolon ( ; ) 
For ex : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="33-34"></code>

But as any languages consists of sub-sentences which combine to make complete sentences, similarly in JS to convey something, we can have a set of expressions which can be complex or simple. 

*To explain fully, if an expression corresponds to sentence fragment, then a statement corresponds to full sentences.*

### 3. Variables:
 
Variables are a way of assigning values, its something we do in our daily lives to make our work simpler. They are simply used to name something so you do not forget.

Now just imagine would it not be weird that everytime if Josh who has curly hair, black eyes, pink lips and short legs would be called as “ I introduce you to the one with the curly hair, black eyes, pink lips and short legs”. Would that really make sense? Would it not be simply easier to say “ i introduce you to Josh”.

That’s why we simply create variables. To remember and to make our lives simpler.

Before we focus on some very simple examples, lets quickly skim through the following pointers. 

- _Variables_ are a storage location pointing to a value associated with an identifier. So, if you are a variable named "Sarah, the girl with curly hair, born in 1990, with the last name George, living in New York", then the long variable in quotes above is the identifier which identifies you. 

- General practice of naming variables is to give a long variable name to those used in computer language, necessitating a description. On the contrary, mathematical variables often have terse, one- or two-character names for brevity in transcription and manipulation. 

- A variable may also be referenced by several different identifiers also. 

> - **Variable declaration :**

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="121-125"></code>

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="36-40"></code>

> - **Variable names:**

A variable name must start with a letter, _ or a $. Anything else would be erroneous. 
 
> - **Rightful and wrongful declaration:**
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="44-48"></code>

 
> - **JS is case sensitive:**
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="49-51"></code>
 
There are words which we can’t use while defining variables because they already exist in the JS environment. 
 
```Var, function, return, class, implements```



### 4. User Interaction:  
a. Alert
b. Console.log
c. Prompt
d. Confirm
e. Comments

 
a. Alert: 

A new small dialog bogs appears on your screen alerting whatever message you alert in the parenthesis. Check out the syntax below and try yourself.
 
Syntax: 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="53-54"></code>
 
b. Console.log: 

This is pretty much works in a similar way, difference it it logs the message in the console that we use to define and declare our JS types etc.
 
Syntax:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="56-57"></code>
 
c. Prompt: 

Prompt allows to ask user to take values from the user input. This is very important to define customized variables.
Prompt asks for two arguments, one, which is the text and the default, which is optional argument, stores the default value in the variable.
 
Syntax:
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="59-62"></code>


d. Confirm:  

It is similar to prompt but instead of a value it stores boolean value in the variable corresponding to the “OK” and “cancel” the user is prompted with. See the following example to understand better.
 
Syntax : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="gistfile1.txt" data-gist-hide-footer="true" data-gist-line="64-65"></code>
