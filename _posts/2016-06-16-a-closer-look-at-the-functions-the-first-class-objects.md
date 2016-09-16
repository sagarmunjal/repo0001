---
published: true
layout: post
---

### 3.1 Syntax

### 3.2 Declaration and Expression

### 3.3 Functions is a value

### 3.4 Self executing functions 

### 3.5 Function naming 

### 3.6 Function Arguments 

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


#### **3.6 Function Arguments 


JS functions can have inner functions. The closure mechanism allows a JS function using variables (except this) from its outer scope, and a function created in a closure remembers the environment in which it was created. In the following example, there is no need to pass the outer scope variable result to the inner function via a parameter, as it is readily available:

```
var sum = function (numbers) {
  var result = 0;
  numbers.forEach( function (n) {
      result = result + n;
  });
  return result;
};
console.log( sum([1,2,3,4]));  // 10
```

When a method/function is executed, we can access its arguments within its body by using the built-in arguments object, which is "array-like" in the sense that it has indexed elements and a length property, and we can iterate over it with a normal for loop, but since it's not an instance of Array, the JS array methods (such as the forEach looping method) cannot be applied to it. The arguments object contains an element for each argument passed to the method. This allows defining a method without parameters and invoking it with any number of arguments, like so:


```
var sum = function () {
  var result = 0, i=0;
  for (i=0; i < arguments.length; i++) {
    result = result + arguments[i];
  }
  return result;
};
console.log( sum(0,1,1,2,3,5,8));  // 20

```

A method defined on the prototype of a constructor function, which can be invoked on all objects created with that constructor, such as Array.prototype.forEach, where Array represents the constructor, has to be invoked with an instance of the class as context object referenced by the this variable (see also the next section on classes). In the following example, the array numbers is the context object in the invocation of forEach:

```
var numbers = [1,2,3];  // create an instance of Array
numbers.forEach( function (n) {
  console.log( n);
});
```

Whenever such a prototype method is to be invoked not with a context object, but with an object as an ordinary argument, we can do this with the help of the JS function call method that takes an object, on which the method is invoked, as its first parameter, followed by the parameters of the method to be invoked. For instance, we can apply the forEach looping method to the array-like object arguments in the following way:

```
var sum = function () {
  var result = 0;
  Array.prototype.forEach.call( arguments, function (n) {
    result = result + n;
  });
  return result;
};
```

A variant of the Function.prototype.call method, taking all arguments of the method to be invoked as a single array argument, is Function.prototype.apply.

Whenever a method defined for a prototype is to be invoked without a context object, or when a method defined in a method slot (in the context) of an object is to be invoked without its context object, we can bind its this variable to a given object with the help of the JS function bind method (Function.prototype.bind). This allows creating a shortcut for invoking a method, as in var querySel = document.querySelector.bind( document), which allows to use querySel instead of document.querySelector.

