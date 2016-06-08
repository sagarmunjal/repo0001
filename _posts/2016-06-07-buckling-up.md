---
layout: post
title: Buckling Up!
date: '2016-06-07 01:51:19 +0530'
categories: javascript basics
published: true
---

1. Buckling up:

    * Setting up the environment
    - Getting to know language
    - Program Structure


---

---

### **Setting up the environment:** 

Google chrome and your workstation. Yes, that’s pretty much all.
We will really set up a proper environment where javascript runs how it gets compiled in a separate post. I would call it a proper environment with some HTML, etc. The google chrome JS console.

---

### **Getting to know the language**

1. Syntax
2. Values


#### 1. Syntax

There are few characters I would want you to see as follows, as they are widely used in JS.

#### Javascript comments : 

They are an awesome way to increase user readability of your code.
JavaScript ignores any statement which starts with “ // “ and the end of the line.

Ex 1:

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="1-2"></code>


#### Multiline Javascript comments : 

Similarly, We can have multiline comments in JavaScript also in which javascript ignore anything between /*  */
Ex 2:

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="4-8"></code>

Semicolons are optional but should not always be ignored:
We write commands in a programming language, these commands are small instructions which are given to the computer called statements. Each statement ends with a semicolon however semicolons are optional after some statements.
 
Ex : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="10-13"></code>

  
Missing semicolon pitfall related to long sentences:
Let’s declare a long variable.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="15-19"></code>
 
This would definitely give out an error because JS compiler treats the above as follows:
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="21-24" data-gist-highlight-line="21"></code>
 
How to evade this error using backslash ( \ )
 
Backslash operator helps us to evade the error by telling the console to ignore the new line.
 
Defining words with single quotes (Another pitfall for beginners ) :
 
Lets define a string:
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-hide-footer="true" data-gist-line="26-27"></code>
 
The above example gives an error because the execution stops after the second single quote at ‘how’
 
To avoid this error we can simply use the backslash.
 
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-line="26,29-30"></code>

<script src="https://gist.github.com/sagarmunjal/9fd0f90a822dc3660cb93703043ca1c6.js"></script>
