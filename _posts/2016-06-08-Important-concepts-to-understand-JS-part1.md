---
published: true
preview: null
layout: post
---
JS: understanding the weird parts

This is not a class to make website or to understand the concepts of this language. 
But this class is about JS. This class is about the where you use JS on the daily basis. 
How JS is nothing like the language called Java, c++, c#. This class is going to help you understnad. You will understand how JS works the way it works, you will find how powerful this language is. 

The biggest mistake that people do while programming is to imitate others without understanding what they are dealing with. 
"so dont imitate, but understand " 

By that I dont mean do not learn from courses or books, but learning from examples that others write you will only be able to get far. Once you will step in the real world and face problems, you will learn by your experience. 

We can compare it by learning any game, by merely learning the rules of a game no one becomes a champion. One has to play the game. Over and again to learn the tips and tricks. 

By playing the game you put yourself at test and gradually learn how to handle different situations with time. 

Also when you deeply understand by taking interest you are able to understand the what's and why's from the others who are performing well. 
You are able to borrow ideas, debug problems and come up with interesting solutions. 




// syntax parser 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtNTN4eHpfTzVoeFU)
so when you write the code it is not magically telling the computer what to do. You are writing code that can be understood by program that someone else made. Here in case of Javascript (when its running in the browser ) it is the JS engine. The JS engine helps you to understand it after converting what you wrote. 

// Compiler / Interpreter
Compiler or interpreter is what converts the language you write to something that computer can understand. This is where the syntax parser also comes in picture as it parses through the code character by character. 

// Scope vs Context explained 

Typically, scope is used to manage the visibility and accessibility of variables from different parts of a program.
Usually, scope is function based and context is object based. 
In detail, scope pertains to variable access of a function when it is invoked and is unique to each invocation. 
On the contrary, Context is always the value of the this keyword which is a reference to the object that “owns” the currently executing code.


// lexical environment or static scoping

![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtNHgzT2x0MThJUlE)

It is where something physically sits in the code you write. Lexical literally means to having to do with words or grammar.
Lexical env exists in a programming language in which where you write something is important. 
In lexical scoping the identifiers refers to its nearest lexical environment.

```
var x = 10;
var y = 20;
 
function foo() {
  console.log(x, y);
}
 
foo(); // 10, 20
 
function bar() {
  var y = 30;
  console.log(x, y); // 10, 30
  foo(); // 10, 20
}
 
bar();
```

In the example, variable x lexically defined in the global scope — that means at runtime it is resolved also in the global scope, i.e. to value 10.

In case of the y name we have two definitions. But as we said, always the nearest lexical scope containing the variable is considered. The own scope has the highest priority and is considered the first. Therefore, in case of the bar function, y variable is resolved as 30. The local variable y of the bar function is said to shadow the same name variable y of the global scope.

However, the same name y is resolved as 20 in case of foo function — even if it is called inside the bar function, which contains another y. I.e. resolution of an identifier is independent from the environment of a caller (in this case bar is a caller of foo, and foo is a callee). And again, this is because at the moment of foo function definition, the nearest lexical context with the y name — was the global context.

Credits/ Reference : [](http://dmitrysoshnikov.com/ecmascript/es5-chapter-3-1-lexical-environments-common-theory) 

// execution context 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtM2traVppYkhsV2s)



// objects: In JS objects are nothing but a collection of key:value pairs. 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtWWFWR0RJQ3prUTA)
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtMzlGa1U3cWJVOGM)

```
address : {stree : 'main',
    number : 110, 
    Apartment : {
      Floor : 3,
      Number : 10
    }
  }
```


// window object (a global default object) & this (keyword which is a reference to the object that “owns” the currently executing code) are two things are created by default.  

// these are the two default objects which are created whenever we open any browser window. 
// so as we discussed in the last class about the execution context and we mentioned about Global object, in case of browsers it is the window object that we are refering to. 

// explanation of window object in browser
Fire up your browser, open up an "about:blank" page and type 'this' keyword in the console and it returns the Window object i.e. the global object which is created by default whenever the browser opens. Hence we know that this here refers to the current execution context i.e. Window object.

```
this   // the keyword this returns the window object. 
```
Now lets define a variable and function in the console. We would be surprised to see that these values are nothing but stored amongst the collection of key value pairs. 
We can even look through the Window object and see that the variable and function we define are stored as key value pairs. 

Let's examine the following example

```
var firstvar = "what the fork!";
function foo(){
console.log('Hey there')
}

// accessing the same variables using this keyword (here this keyword references to Window Object)
this.firstvar; // this returns the variable "what the fork!" 
this.foo;      // this returns the function definition function foo(){console.log('Hey there')}

// the code above can be accessed thorugh the window object, this is an evidence that they are stored as a property in the Window global object
window.firstvar;  // this returns the variable "what the fork!" 
window.foo;       // this returns the function definition function foo(){console.log('Hey there')}
```
