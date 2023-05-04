# Regex-Tutorial

## Summary
This is a tutorial breakdown on how Regex is used to match a Hex Value in a body of text. 
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` is the syntax that I will be using. 

Hex Code is a way to identify color. It is always in a 6-digit alphanumeric sequence. 

The regex string I am using will return a # Number sign character followed by either a 6 or 3 character length code with only lowercase letters a,b,c,d,e,or f or numbers 0,1,2,3,4,5,6,7,8, or 9. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors
The starting ^ caret and ending $ dollar sign are both anchors in the example string. 
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

* The ^caret matches at the start of the string the regex pattern is applied to.
* The # Number Sign following the starting ^caret is a literal character and a #Number Sign **MUST** be at the start of the string. 
* The $ dollar sign matches at the end of the string the regex pattern is applied to. This signifies the end of the string. 


### Quantifiers
Each quanifier denotes how many times the previous token will be matched. 
There are 3 quanitfiers in the example syntax. 
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

1. The first $ Dollar Sign ( which I will also go over in the Greedy section)
   This signifies that the # Number Sign will match 0-1 times. 
    
2. {6}
   This signifies that the previous token [a-f0-9] will have 6 characters match within that set.
    
3. {3}
  This signifies that the previous token [a-f0-9] will have 3 characters match within that set.

### OR Operator
The example syntax uses an OR operator known as | Vertical line or pipe. 
There is a | Pipe between two characters classes. This creates 2 alternative groups. This allows the search to find and match either group. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
* The first alternative is before the | pipe [a-f0-9] will return 6 characters. 

* The second alternative after the | Pipe will return 3 characters. 

### Character Classes
Character classes are found betwen [...] square brackets. They are used to create a list of allowable characters. 
In the example syntax there are two character classes. They look exactly the same because they are, however the **quantifier** is what makes each class return a different number of characters. 

The example uses [a-f0-9]
* a-f = This is the range that matches a case sensitive single character of:  a,b,c,d,e, or f.  
* 0-9 = This is the range that matches a case sensitive single digit of: 0,1,2,3,4,5,6,7,8, or 9

### Grouping and Capturing
Anything found inside of ( round brackets ) creates a capture group. Everything inside that (...) is treated as a single unit. 
So with the example syntax 
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
there is one capture group with two characters sets seperated by an OR Operator.

### Greedy and Lazy Match
Remember the ? quantifier we talked about earlier? 
The single ? by defult is considered greedy. This means it will match as many occurrences of the given pattern as possible.
A lazy match would be denoted as a double ??.  Lazy means as few occurrences of the pattern as possible, however our example syntax is considered greedy not lazy. 

### Boundaries
Boundries used are the ^caret to siginify the start of the string and the $ dollar sign signifies the end of the string.

## Author
Hey there! I am Andre, at UCR Full Stack Developer Bootcamp student. This assignments is to learn about Regex and gists. Read my Regex tutorial., at my [Gist-Github](https://github.com/Dre0239/Regex-Tutorial/blob/main/.gist.js) 


