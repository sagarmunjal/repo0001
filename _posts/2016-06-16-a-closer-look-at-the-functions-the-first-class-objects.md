---
published: true
layout: post
---

### 3.1 Syntax

### 3.2 Declaration and Expression

### 3.3 Functions is a value

### 3.4 Self executing functions 

### 3.5 Function naming 

---
---
---

In javascript functions are first class objects. What do we mean by that?

Think of your favorite  super hero, now obviously if there are ten people every one can have a different favorite superhero. But just imagine, there is one _SUPER_ superhero, who does the jobs of all superheroes. That's what functions are in Javascript and to attain limitlessness while unleashing the power of functions we have to understand them very acutely. 

Let's look at the following pointers, how functions are special type of objects: 

- A function is an instance of an Object type. 
- A function can have properties and can have a link back to it's constructor function. 
- Functions can be stored in a variable
- Functions can be passed as arguments to other functions
- You can return function from another functions 

Well, all the above information is too overwhelming, yes a fair amount of knowledge would help you float your boat but maybe you will find yourself at sea if you just landed here without any prior knowledge. But do not worry, we will explain things in detail below and help you with how functions are the first class objects by end of this chapter. 

Being JS objects implies that JS functions can be stored in variables, passed as arguments to functions, returned by functions, have properties and can be changed dynamically. Therefore, JS functions are first-class citizens, and JavaScript can be viewed as a functional programming language.

The general form of a JS function definition is an assignment of a JS function expression to a variable:

```
var myMethod = function theNameOfMyMethod( params) {
  ...
}
```

where params is a comma-separated list of parameters (or a parameter record), and theNameOfMyMethod is optional. When it is omitted, the method/function is anonymous. In any case, JS functions are normally invoked via a variable that references the function. In the above case, this means that the JS function is invoked with myMethod(), and not with theNameOfMyMethod(). However, a named JS function can be invoked by name from within the function (for recursion). Consequently, a recursive JS function must be named.


#### **3.1 Syntax**

> - SYNTAX 1 : FUNCTION DECLARATION

```
function f(arg1, arg2, ...) {
   ... code block ...
}

Ex : 
function sum(x,y) {
return x+y;
}

```

> - SYNTAX 2 : FUNCTION EXPRESSION

```
var f = function(arg1, arg2) { 
... code block ... 
}

Ex : 
var sum = function (x,y){
return x+y;
}

```

> - SYNTAX 3 : By usning the "new Function" keyword
var f = new Function('arg1,arg2','...code block ...')

Ex : 
var sum = new Function ('x,y', 'return x+y')

---

#### **3.2 Declaration and Expression**

The concept of declaration and expression is very important to understand on the basis of the literal jargon used in programming world. 

We will briefly recapitulate few definitions : 

_Expression_ is a small fragment of code that produces a value and is dependent on other expressions. Expressions are analogous to clauses in english, the clause never makes complete sense until used in a complete sentence. 

_Statement_ is a small group of expressions that performs an action altogether and is independent in nature. So yes, as per our understanding we can say that many expressions come together and make up a statement. 

_The only thing ECMA specs make clear is that Function Declaration must always have an Identifier (or a function name, if you prefer), and Function Expression may omit it_

> - Functions Declarations always gets parsed in the pre-executing state, when the browser is preparing itself

```
sum (6,3)

function sum (x,y){return x+y} // the function will still be executed despite of being declared after it has been called

```

> - Function Expression is just like a value like other numbers or string

Function expression unlike declaration do not get parsed in the pre-executing stage, they only get parsed after they have been defined. 

```
sum (6,3)  // gives an error

var sum = function (x,y){ return x+y}  // Function expression 

sum (6,3) // outputs the result because the function call has been made after the 
```

> - When a function means a declaration and when an expression?

The logic is simple, that when the javascript parser sees the function in the main code flow it's a declaration and when the function is part of a statement its an expression.


---

#### **3.3 Functions is a value**

Like any other value, functions are also values. 

> - We can out a function like any other value

```
var x = "this is a string " ;

alert(x) ; // alerts the string x

function foo () {alert("This is a function")};

alert (foo ) ; // alerts the function foo

```

> - Just like any other value it can be assigned to other variables : 

```
function sum(x,y) {
return x+y;
}

var addtwonumbers = sum;

addtwonumbers(7,8) // outputs the sum

```

---

#### **3.4 Self executing functions**

Self executing functions are those which execute immediately and automatically after its definition. 

```
SYNTAX 1 : SELF EXECUTING FUNCITION

(function sum (x,y){return x+y})(4,6) // outputs the sum immediately after its execution

SYNTAX 2 : SELF EXECUTING FUNCITION

var sum = function (x,y){ return x+y } (4,6) // outputs the result again

```

In the above mentioned lines of code, did you notice some difference?

Yes, the first difference is that SYNTAX 1 requires parenthesis around the function. why?

That's because if the function will not be wrapped by the parenthesis, the javascript parser will notice the keyword function and treat is as a function declaration but will throw an error. It will not make sense for the javascript parser to interpret what does the following parenthesis enclose i.e. (4,6)

In order to help javascript parser treat the function declaration as a statement we have to wrap it in paranthesis. 

However, in SYNTAX 2, when we have declared the statement we do not need the parenthesis, because javascript already treats it as a statement. 

---


#### **3.5 Function naming**

A function is always an action that is being performed, so the name should always be a verb such as calculateSum, calculateArea, product, etc. 


---
