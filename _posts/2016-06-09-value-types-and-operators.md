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
+, -, , /, %.
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

> - **Postfix**

> - **Prefix**



### 4. Bitwise Operators

These are obsolete operators and are rarely used, but there are few hacks that we might want to have a look at. 
 
For a detailed summary on bitwise operators refer (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators#(Bitwise_AND))
 
And (&)
Or  (|)
Xor (^)
Not (~)
Left shift 	(<<)
Right shift (>>)
Zero fill right shift (>>>)
 
One of the exception of bitwise operator is the not operator. ( ~ )

> -Smart use of bitwise operator:

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="28-37"></code>


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

a. OR ( || )

Logical OR is an important choice when you have multiple operands and want to print the first value which is true.

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="48-53"></code>

b. AND ( && )

Logical and operator check the first operator if its true and then also checks the second operator.

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="56-61"></code>

c. NOT ( ! )

Not operator turns the operator into boolean value and negates it.
<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="65-71"></code>



### 6. Assignment operators

```
> = , += , *= , /= , >>= , <<= , >>>= , &= , |= , ^=
```

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="74-78"></code>
---

#### **2.3 Comparison Operators** 

The if… else code checks for conditions and runs the code if it’s true or false
 
Most well known comparison operators ar
e : 

> ==, <= , >= , < , >

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="81-87"></code>

It is also possible to specify additional condition using else… if…

---

#### **2.4 Loops and Switches**

a. The while and do...while loops
b. The for loop
c. Jumping out with breaks
d. Skipping with continue
e. Jumping over blocks with labels
f. The switch construct

a. The while and do...while loops

It checks the condition before and every iteration

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="89-98"></code>
 
The only difference between while and do while loop is that the latter executes at least once.

b. The for loop

The for loop consists of a condition within parenthesis, with three pars and a separate body to be executed.
 
It looks like this

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="100-104"></code>

 
The condition part consists of three parts,
- One is the *variable* and the initializing of the variable.
- Second is the *condition*
- And third is the *increment or decrement expression*

<code data-gist-id="9fd0f90a822dc3660cb93703043ca1c6" data-gist-file="chap2.txt" data-gist-hide-footer="true" data-gist-line="105-108"></code>

Now the above example alerts x, starting from x = 0 and loops until the condition fails while x =10 and terminates at x = 10.
