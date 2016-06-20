---
published: true
layout: post
---

### 4.1 Strings

### 4.2 Number, Math

### 4.3 Objects

### 4.4 Arrays

---

---

---

## **4.1 Strings**

> - **How to create strings**

Strings can be simply declared in single or double quote

```
var newString = "thisisanewstring"

var multilinestring = "this is a multiline string \
this is next line of the string \
this is the last line"

```

There is no difference between a double quote and a single quote.

special characters : 
\b - Blankspace
\n - Newline
\f - Formfeed
\t - New tab
\r - Carriage return 


> - **Methods and Properties**

a. String.length : helps us to get the length of the string. 

```
var str = "this \n is next line \t and this is a tab " // all the special character and white spaces count as 1 character.


```

b. Strig.charAt

```
var str = "hello lets access the characters in the string
str.charAt(0) // outputs 'h'

var newstr = str.charAt(0) + str.charAt(4) + str.charAt(8) // manipulating string
```

c. Lowercaser/ Uppercase conversion

```
var str = "juno is my name"
str.toUpperCase() // outputs "JUNO IS MY NAME"

str.charAt(0).toLowerCase() // outputs "jUNO IS MY NAME"
```

d. Finding a substring using indexOf method : 
This method returns the position of the first instance of the matching instance. 
Similarly lastIndexOf method searches the string from the end instead from the beginning. 

```
var str = "boozo is the dog and his instram page link is www.instagram.com/ziggieboozo "
str.indexOf('www')

str.indexOf('boozo') // returns 0 as it checks from the beginning
str.lastIndexOf('boozo') // returns 71 as it checks from the last

```

e. Extracting a substring

We would be learning about three methods here
substr, substring, slice

_substring(start [, end])_ Method substring(start, end) extracts a substring from start to, but not including position end. The count starts from 0.

```
var str = "boozo is the dog and his instram page link is www.instagram.com/ziggieboozo "
str.substring(0) // omitting the second parameter in the method means that it will go till the end
str.substring(0,12) // outputs "boozo is the"
str.substring(5,12) // outputs " is the"
```

_substr(start [, length])_ The first argument is same as in substring, but second argument is “how many characters to extract” instead of ending position.

```
var str = "boozo is the dog and his instram page link is www.instagram.com/ziggieboozo"
str.substr(0) // omitting the second parameter in the method means that it will go till the end
str.substr(0,12)  // outputs the same as above "boozo is the"
str.substr(5,12) // outputs " is the dog and "
```


_slice(start [, end])_
Returns a portion of the string from position start to, but not including position end. That’s same as substring.
Slice method is same as substring except that they treat negative values differently. Let's see in the examples below. 

```
var str = "boozo is the dog and his instram page link is www.instagram.com/ziggieboozo"
str.slice(0)  // omitting the second parameter in the method means that it will go till the end
str.slice(0, 12 ) // outputs the same as above "boozo is the"

str.slice (-10) // it starts from the last character treating it at a position -1 and goes till the end if the second param is omitted.

str.slice(-10, -1 ) // this means it will now start with the -10th character from the last and go till 
-1 character
```


> - **Comparison**

Strings are compared lexicographicaly.

which means the following

```
"s1" < "s2" // outputs true
"S1" < "S2" // outputs true
"S1" < "s2" // outputs true
"s1" < "S2" // outputs false because Uppercase is always smaller in value than Lowercase
"ss" < "sss" // outputs true because a character less always decreses the value
```



---

## **4.2 Number, Math**

JS datatype numbers include floating point decimals, but there may or may not be a fractional component. If they do not have a fractional componenet they are treated as integers, which range from -2^53 to 2^53


```
// The following are valid integers:

var negativeNumber = -1000;
var zero = 0;
var fourDigits = 2534;
```

The floating-point representation has a decimal, with a decimal component to the right. You also can represent the number as an exponent, using scientific notation. 

```
// All of the following are valid floating-point numbers:
var someFloat = 0.3555
var anotherNumber = 144.006;
var negDecimal = -2.3;
var lastNum = 19.5e-2 //which is equivalent to .195
var zeroDecimal = 12.0;
```

> - **Two special type numbers are Infinity && negative Infinity**

Any interger or floating point divided by 0 results in Infinity. 

```
// Infinity

var x = 10/0
console.log(x)

// negative-Infinity

var x = -10/0
console.log(x)

```

> - **Written forms**

In Javascript we can have many ways to represent numbers
Hexadecimal 
Octal
Scintific notation

Hexadecimal and Octal representation

```

alert( 0xFF ) // 255 in hexadimal form, starts with 0x
alert( 010 ) // 8 in octal form, starts with 0

```

Scientific notation : 

```
// scientific form: 3 with 5 zeros
alert( 3e5 )  // 300000
alert( 3e-5 ) // 0.00003

```

> - **NaN**

If an operation can't be performed then it returns a pseudo numeric value i.e. NaN

A NaN value is not even equal to itself. 

```
console.log( 0/0 ) // returns NaN
console.log( NaN == NaN) // returns false
console.log( NaN === NaN ) // returns false
```

An operation which returns a NaN or not can be checked using the "isNaN" method. 

```
x = 0/0;
console.log(isNaN(x)); // returns true
```

> - **Conversion to a number**

We can simply convert strings of numbers to numbers using the (+) plus operation.

```
var s = "12.34"
console.log( +s )  // 12.34

alert( +"  12")  // 12
alert( +" \n34  \n") // 34, newlines are whitespace symbols too

alert( +"12test" )  // if a number cant be converted then it returns "NaN"


```

> - **Permissive String conversion using : parseInt and parseFloat**

Usually there are a lot of times when we need to convert strings to numbers such as "12px" used in CSS, etc. 

parseInt and its friend parseFloat convert the value character by character until they meet something impossible to convert. Then it stops and returns what could be converted.

```
alert( parseFloat('12.3.4') ) // 12.3, 1st dot is fine, but not the 2nd


alert( parseInt('0xFF') ) // 255
alert( parseInt('010') )  // in some browsers 8, because 0 means octal

alert( parseInt('010', 10) ) // If you want be sure that “010” means 10, use the second optional argument to pass the radix

alert( parseInt('a123') ) // Note, parseInt/parseFloat returns NaN if conversion stops at first char:

```

> - **Rounding**

a. Math.floor - Rounds down
b. Math.ceil  - Rounds up
c. Math.round - Rounds to nearest


```
alert( Math.floor(3.1) )  // 3
alert( Math.ceil(3.1) )   // 4
alert( Math.round(3.1) )  // 3

```

Note the behavior of the three methods on negative integers. 

```
alert( Math.floor(-3.1) )  // -4, rounds to nearest less than -3.1
alert( Math.ceil(-3.1) )   // -3, rounds to nearest greater than -3.1

```

> - **Math.random**

Math.random alerts a number between 0 and 1. 

```
console.log(Math.random())
```
---



## **4.3 Objects**



---

## **4.4 Arrays**
