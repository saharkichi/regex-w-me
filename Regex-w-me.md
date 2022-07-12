# Regex-w-me

This is a tutorial that explains how a specific regular expression, otherwise known as regex, functions by breaking down each part of the expression and describing what it does. As a web development student, a tutorial explaining a specific regex will help students understand the search pattern the regex defines

## Summary

To gain a better understanding of how regular expressions are created, I have chosen a regex code that matches an HTML tag. The code that I will be describing is as follows: <br>
Matching an HTMl tag: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)

## Regex Components

A regex is a sequence of characters that defines a search pattern within a body of text. Each character involved in a regex is defined as a literal character. We will be breaking down each character involved in the HTML tag regex and dividing them into their appropriate components. The components involved in the code we are depicting in this tutorial are as follows: 

### Anchors

We see two anchors at the beginning of the regex and the end. 
The forward slash / and the back slash \ at either end of the expression are indicating the start and the end of the expression, however they are not defined as anchors. 
<br>
<br>
The first anchor in the expression is ```^``` <br>
This is called the caret anchor which asserts that the engine's current position in the string is the beginning of the string, or the beginning of the line if the multiline flag (m) is enabled. An example of this would be ```^abc``` identifying that ```abc``` is appearing at the start of the string or line. 
<br>
<br>
The last anchor in the expression is ```$```<br>
This is called the dollar anchor which matches the end of the string, or the end of the line if the multiline flag (m) is enabled. An example of this would be ```xyz$``` identifying that ```xyz``` is appearing at the end of the string or line.

### Quantifiers
There are two main quantifiers used in this regex expression. Quantifiers allow you to declare quantities of data as part of your pattern.
<br>
<br>
Firstly, we have ```+``` which matches one or more of the preceeding token. An example and an equivalent expression would be ```{1,}``` This is an example of a greedy quantifier because they cause the regular expression engine to match as many occurrences of particular patterns as possible.
<br>
<br>
Lastly, we have ```*``` which matches zero or more of the preceeding token. An example and an equivalent expression would be ```{0,}``` This is an another example of a greedy quantifier. 

### Grouping Constructs
Grouping can allow you to match a subexpression that is repeated in the input string, apply a quantifier to a subexpression that has multiple regex language elements, or to treat another expression as a single unit. 
<br>
<br>
In the example we are looking at, we see 3 different captured groups. 
<br>
<br>
Firstly, we see capturing group 1 which is shown as ```([a-z]+)``` It groups multiple tokens together and creates a capture group for extracting a substring or using a backreference. Within this group we see an example of a bracket expression which will be discussed next, and an example of a quantifier which was previously discussed.
<br>
<br>
Secondly, we see capturing group 2 which is shown as ```([^<]+)```. It also groups multiple tokens together and creates a capture group for extracting a substring or using a backreference. Within this group we see an example of another quantifier, and an example of a negated set which will be discussed next. 
<br>
<br>
Thirdly, we see capturing group 3 which is shown as ```(.*)``` It has the same attributes as the previous capturing groups but also includes a quantifier and a dot which has not yet been discussed.
<br>
<br>
Lastly, we see an example of a non-capturing group which differs from the previous capturing groups discussed. We see this here ```(?:>(.*)<\/\1>|\s+\/>)``` The non-capturing group groups multiple tokens together without creating a capture group such as the examples above. Within this non capturing group, we see capturing group3, a dot, multiple quantifiers, and characters that will be further discussed.

### Bracket Expressions
A bracket expression is a list of characters enclosed by '[' and ']'. It can match any single character in that list. 
<br>
<br>
We see the first bracket expression within captured group 1 as ```[a-z]``` This demonstrates a range which matches a character in the range "a" to "z" and it is case sensitive. This also demonstrates a positive character group. For example purposes, ```[a-d]``` is equivalent to ```[abcd]```
<br>
<br>
We see the second bracket expression within captured group 2 as ```[^<]``` This is referred to as a negated set, which matches any character that is not in the set. This demonstrates a negative character group.

### Character Classes
The fundamental classes of character are "word" characters (such as numbers and letters) and "non-word" characters (such as spaces and punctuation marks).
<br>
<br>
We see the ```.``` Dot. character within captured group 3. This matches any single chracter except the newline character including line breaks. 
<br>
<br>
We also see the ```<``` character multiple times which matches a "<" character or ```>``` which matches a ">" character. 
<br>
<br>
We also can see an example of a whitespace character here ```\s``` This matches any whitespace character including spaces, tabs, and line breaks. This differs from another common whitespace character such as ```\s+``` because it only represents a single whitespace character while the latter represents multiple whitespaces in a string.

### The OR Operator
To achieve the "or" operator, we can use grouping and/or alternation. 
<br>
<br>
We see examples of this within our code such as the pipe character and/or alternation which we see depicted as ```|``` This character seperates terms contained within each group. This can also act like a boolean OR operator and it matches the expression before or after the ```|```
<br>
<br>

### Character Escapes
We see two uses of the same escaped character which looks like ```\/``` This matches a "/" character. 
<br>
<br>

Since most escaped characters begin with ```\``` we see another example of this in the code as ```\1``` This is a numeric reference which matches the results of capture group #1

## Author

This was written by Sahar Kichi. A new and aspiring full stack web developer. She created this tutorial to not only use as a cheatsheet for herself, but to help others aswell. 
[Github Profile Here](https://github.com/saharkichi)

