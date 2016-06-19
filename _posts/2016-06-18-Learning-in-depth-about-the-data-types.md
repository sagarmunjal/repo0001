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

---

## **4.3 Objects**

---

## **4.4 Arrays**
