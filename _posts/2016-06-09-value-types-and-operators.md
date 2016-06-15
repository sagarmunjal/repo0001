---
published: true
layout: post
---
### 2.1 Value types

### 2.2 Operators

### 2.3 Comparison Operators

### 2.4 Loops and Switches

---

---

---

#### **2.1 Value types** 

> - Number

All numbers like 0,3.4 and also pseudo-numerical values like NaN and Infinite.

> - Strings

“Meow”

> - Boolean

True and false values.
                
> - Null, undefined

Special values

> - Objects 

Other values like functions, arrays are objects

_To be honest, the types are complicated to explain because really there are Functions, Arrays, Date, RegExp which also fit somewhere in the tree above. But for now lets just keep it as simple as it’s shown above._

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="2-10"></code>



---

#### **2.2 Operators** 

1. Arithmetic operators
2. String Concatenation
3. Increment/ Decrement
4. Bitwise Operators
- Smart integer operations
5. Logical operators
6. Assignment operators


### 1. Arithmetic operators 

Arithmatics means maths, and here we are talking about simple highschool maths. 

```
+, -, , /, %
```

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="11-15"></code>

The percentage operator is called the modulus operator and it returns the remainder.

```
i = 5 % 2; // 1
i = 8 % 3; // 2
i = 6 % 3; // 0
```


### 2. String Concatenation

_Concatenation_ in simple english means to join or link together to form a chain or series. 

``` var jointhesewords = "joining" + "the" + "strings" ;
```

> - **If one of the operand is string then the other operand is also treated as a string;**

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="18-21"></code>

### 3. Increment/ Decrement
These are the two increment and decrement operator and they change the variable value itself.
We can simply call them as plus 1, denoted as ++1 and subtract 1 denoted as --1. 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="22-27"></code>

The postfix and prefix of the operator returns different values.

> - **Postfix (i++)**

The postfix operator returns a value and then increments. 

> - **Prefix (++i)**

The prefix operator increments and then returns the value

<code data-gist-id="4c11fe53e8066aa419103bcf51d88d38" data-gist-hide-footer="true" data-gist-line="1-14"></code>


### 4. Bitwise Operators

These are obsolete operators and are rarely used, but there are few hacks that we might want to have a look at. 
 
For a detailed summary on bitwise operators refer (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators#(Bitwise_AND))
 
```
And (&)

Or  (|)

Xor (^)

Not (~)

Left shift 	(<<)

Right shift (>>)

Zero fill right shift (>>>)
```
 
One of the exception of bitwise operator is the not operator. ( ~ )

> - **Smart use of bitwise operator:**

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="28-37"></code>

> - **Practice Yourself**

<code data-gist-id="4c11fe53e8066aa419103bcf51d88d38" data-gist-hide-footer="true" data-gist-line="16-37"></code>


### 5. Logical operators

a. OR ( || )

b. AND ( && )

c. NOT ( ! )


```
alert( true && false ) // false
 
alert( false || true ) // true
 
alert( !false ) // true

```
> - **Values that have a boolean value false, no matter what:**

There are few values like an empty string ( "" ), 0 and special values like null and undefined. 

> - **Logical operators can be applied to even non-boolean values:**

A logical boolean operator can be applied to anything and in case of a non boolean value, in order to evaluate its value it is converted into a boolean value.


These are short circuit  operators.
For eg:

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="40-44"></code>

a. OR ( | | )

Logical OR is an important choice when you have multiple operands and want to print the first value which is true.

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="48-53"></code>

b. AND ( && )

Logical and operator check the first operator if its true and then also checks the second operator.

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="56-61"></code>

c. NOT ( ! )

Not operator turns the operator into boolean value and negates it.
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="65-71"></code>

> - **Practice Yourself**

<code data-gist-id="4c11fe53e8066aa419103bcf51d88d38" data-gist-hide-footer="true" data-gist-line="40-50"></code>



### 6. Assignment operators

```
>= , += , *= , /= , >>= , <<= , >>>= 
```

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="74-78"></code>

> - **Practice Yourself**

<code data-gist-id="4c11fe53e8066aa419103bcf51d88d38" data-gist-hide-footer="true" data-gist-line="52-63"></code>

---

#### **2.3 Comparison Operators** 

The if… else code checks for conditions using the _comparison operators_ and runs the code if it’s true or false. On the basis of the result being true we move on to the next code block. 

It is simple to understand by an analogy, if you have solved the question and the condition is true then drink your beer or else finish your assignment. 
 
Most well known comparison operators are : 

```
==, <= , >= , < , >
```

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="81-87"></code>

Next we will discuss the loops and switches which make use of the comparison operators. 

---

#### **2.4 Loops and Switches**

In life we often come across real time situtions in which we have to look for an answer by performing a similar set of task under certain condition. 

For ex : If my gf wants to have strawberry cheese cake, and I have ten bakeries namely bakery1, bakery2 and so on.  

Now, I will go to each bakery ( bakery1, bakery2, and so on...)  until I find the cake.

Similarly, we use the above mentioned comparison operators combined with loops to achieve certain results in the programs that we write. 

```
a. The while and do...while loops

b. The for loop

c. The switch construct
```


a. The while and do...while loops

These are two types of while loops and there is a slight difference between them.  
Let's have a closer look towards their execution. 

> - **WHILE LOOP**

```
SYNTAX : 
while (condition) {
    code block to be executed
}
```

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="112-114"></code>

> - **DO WHILE LOOP**

```
SYNTAX : 
do {
    code block to be executed
}
while (condition);
```


<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="116-121"></code>
 
The only difference between while and do while loop is that the latter executes at least once.

b. The for loop

The for loop consists of a condition within parenthesis, with three parameters and a separate body to be executed.
 
It looks like this

```
// SYNTAX
for (x = 0 ; x < 10 ; x ++){
// do something
}

```
 
The condition part which is enclosed in the parenthesis ( ) consists of three parts as follows : 
- One is the *variable* and the initializing of the variable. In the above example it is denoted by x = 0. 
- Second is the *condition*. This condition is to tell the loop to keep executing till this condition is true. 
- And third is the *increment or decrement expression*. Increment or Decrement operator is applied to 'x' so that the loop ends after the condition is false. 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="105-108"></code>

Now the above example alerts x, starting from x = 0 and loops until the condition fails while x =10 and terminates at x = 10.


> - **Practice Yourself**

```
Question 1 : Write a for loop to log "the number is 50 and is even" for all even numbers and "the number is 51 and is odd" for all odd numbers for numbers between 50 to 70. 

Question 2 : write table of 9 and log the table of 9 in the format " 1 * 9 = 9 " , " 2 * 9 = 18 " upto " 10 * 9 = 90 ". 

Question 3 : Now using the above method of logging table of 9, log tables from 1 - 10 in the same format. 

```

> - **Jumping out with break**

_Infinite loops_ are loops which iterate infinitely because the condition mentioned is always true. 

For ex : 

```
// This is an infinite loop 
var i = 0 ; 
while (true){
console.log(i ++ )
}
```

Infinite loops which run eternally can be stopped by using the break statement as follows. 

```
// Applying breaks to an infinite loop 
var i = 0 ; 
while (true){
console.log(i ++ )
if (i>5) break
}
```

c. Switch statements : 

Switch statements work under certain case value pairs. See the syntax below for better understanding. 


```
switch(x) {
  case 'value1':  // if (x === 'value1')
    ...
  case 'value2':  // if (x === 'value2')
    ...
  default:      
    // default code
}
```

Lets see at a working example of switch statement : 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="133-147"></code>

The above example has a flaw that it does not use "break; " statement after the second case and hence all the cases after the second case are executed. 
We can simply stop that by using a break statement as shown below. 


<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="152-167"></code>

This is a simple user input example of a switch statement. 

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="174-194"></code>

