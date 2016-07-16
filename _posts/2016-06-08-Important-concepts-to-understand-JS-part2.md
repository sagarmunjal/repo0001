---
published: true
layout: post
---
// The execution context : creation and hoisting 

![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtMWZ3U3JHOUNlNzg)

The reason that js behaves the way it does, that functions and variables are available even when they are written later in the code because their execution context is created in two phases.
the first phase is called the "creation phase"
While in this creation phase when the syntax parser goes through the code it recognizes where you have created variables and where you have created functions.
So it sets up memory space for Variables and Functions "Hoisting "

```
// case 1 : 
var a = 'fork the world';
console.log(a);

// case 2 : 
console.log(a);
var a = 'fork the world';

```
// case 1 : 
We see that we log the value of a and get the value 'fork the world'. Fair enough, eh!
// case 2 : 
// The var a comes out to be undefined. Not so fair! Because the JS syntax parser firstly scans all the variables and allocates them memory. Just think about it this way, that it simply keeps them in memory as of yet and just knows that they do exist.
Now, JS runs the code one line after other. So the value of var a in case2 is replaced by a placeholder value i.e. undefined until it reaches the line where var a is assigned a value. 

//Hoisting : 
This is what is called hoisting. When a variable exists in the memory but its value is still undefined.
Functions on the contrary are sitting in the memory in its entirety. Yes, they are different than variables.

```
case 1 : 
function foo(){console.log('this is something')}
foo();

case 2 : 
foo();
function foo(){console.log('this is something')}
```
Here, it hardly matters that if the function is invoked before or after the function definition, thats because when the memory space is being taken up, then the all the function definitions are also stored in it. Hence the function can be invoked anywhere in the code. 


```
//case 1 
console.log(a) // gives an error

// case 2 
console.log(a) // gives undefined
a = 10;

// case 3 
a = 10 ; 
console.log(a) // gives value 10 
```
undefined : Does not really mean not defined. Yes, it's confusing but do not get confused. 
As a matter of fact undefined just means that the variable exists but the value of the variable does not. Simple right? Keep reading it until you understand.

Uncaught ReferenceError: a is not defined : This is what means that the value does not even exist and it needs to be declared or defined to fix this error. 


// test that undefined is really a value in stored in JS engine 
```
console.log(a);
var a;
if(a===undefined){console.log('a is undefined')}else{console.log('a is defined')}
```
//Now we discuss the use cases of declaring and assigning value to a variable inside the global scope and inside a function

```
case1 : when variable a is not defined inside the function body and only in global lexical environment.

var a = 10 ;

function foo () {
console.log(a) 
}

console.log(a);  // 10
foo(); // 10

case 2 :  when variable a is defined inside a function body also
var a = 10 ;

function foo () {
var a = 20;
console.log(a)

}

console.log(a);  // 10
foo(); // 20

case 3 : when var a is only declared in the function body but not assigned a value. 
var a = 10 ;


function foo () {
var a;
console.log(a)
}

console.log(a);  // 10
foo(); // undefined

```

// above we discussed the first phase as the creation of memory space. phase, the second phase is the execution phase. 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtWFBLRDF2d3A4c3M)

//single threaded execution 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtYUNuWXJSSUtmaHM)
This means that JS executes command one at a time. In browsers JS may not seem to be single threaded but from our perspective as developers its single threaded language.

// Synchronous execution 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtdDlEN2FjN0V5cW8)

// function invocation 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtZXZWelctYWRWbWM)


```
function b() {}
function a () {
b()
}
a();
```
// Discussing creation of the execution context stack. First lets discuss a simple example. 

Now in the above example we have function b defined, function b invoked inside function a definition and function a invoked. 
So first global execution context is created along with a special variable 'this'.
And then it will make memory space in the creation phase for these functions that we have defined. 
And then the code will be executed in the execution phase line by line.



![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtTGxkM3ZJZ2p5QUE)
//lets understand variable environment
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtLUhDSUlleHRyalE)

Let's use console.log to see different values and understand practically and we will also discuss what is variable environment. 
```
function b() {
    var ax = 30;
    console.log(ax);
}
function a() {
    var ax = 10;
    console.log(ax);
    b()
}

var ax = 20;
console.log(ax)
a();

```
The above execution context and variable environment can be understood by following chart. 
in which we will discuss the execution context along with the respective variable environment.

Execution stack  ( Creation and execution )
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtU19PUE1OVFpkZDg)

Scope Chain 
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtMjMyTkc4VU5oWnM)


To understand scope chain first lets clearly understand what does reference scoping mean : 

```
function b() {
    console.log(x1)
}
function a() {
    var x1 = 'somevalue'
    b()
}
var x1 = 'anothervalue'
a();


```
![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtS0RaY3VUUHl0dVE)

Now, in the above example we can see lexical environment in action. Even though execution context b() sits directly above a(). It is sitting at the same level as a that is the global object. 
Also, we discussed that if function b does not have a value of a variable defined, it goes up and checks in its reference to the outer environment. Here the outer environment just above b() is the window object and the value of the variable in the window object is anothervalue. Hence, it console.logs 'anothervalue'


Now we will modify the above example a little bit and see how the result changes. 
```
function a() {
    var x1 = 'somevalue'
    b()
    function b() {
        console.log(x1)
    }
}
var x1 = 'anothervalue'
a();
```

Now, we have defined b() inside function a() and we know that we have var x1 defined at the execution context of a(). So now when, b() gets invoked and it asks to console.log value of x1, it consoles.log "somevalue" instead of "anothervalue". 
This is because now the reference to the outer scope has changed to a() rather than the global execution context. So the value of x1 becomes what is defined inside the body of function a() i.e. "somevalue".

```
function a() {
    b()
    function b() {
        console.log(x1)
    }
}
var x1 = 'anothervalue'
a();
```

Now, if in the case above if value is not defined in the body of function a() also, then the value again is picked from the reference to the outer environment. So, going down the chain of reference to the outer environment until it gets value of x1 defined. This chain is called the scope chain. 



```
third();
var x3 = 'x3'
function third() {
    var x2 = 'x2'
    second()
    function second() {
        var x1 = 'x1'
        first()
        function first() {
            console.log(x1,x2,x3)
        }
    }
}

```
In the above section we have explained, reference to the outer environment and scope chain. 

![](https://drive.google.com/uc?export=view&id=0B8kNn6zsgGEtUWt0Y1VCOEpsUmM)