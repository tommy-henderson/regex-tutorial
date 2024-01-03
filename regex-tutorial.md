# Regex Tutorial 

The purpose of this tutorial is to help understand regular expression (Regex) using an example.

## Summary

This tutorial will utilize the following code which is used for matching emails:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This code can make sure that an email address follows a specific formula

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

The Anchor is what begins and ends the expression. In our example, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, the anchors are the caret (^) and the dollar-sign ($).
The code is looking for something that starts with the characters directly after the ^. In our example it is the following string:
^([a-z0-9_\.-]+)

It is also looking for something directly before the $. In our example it is this string:
.([a-z\.]{2,6})
If it does not meet these parameters, it will not be a match.

### Quantifiers

Quantifiers are used to see how many times certain characters or strings need to be present to constitute a match. Our code contains the "+" quantifier which says that it has to contain at least one in order to match. 

### OR Operator

The OR operator is signified by the character: "|". This means that the string can set 2 terms and will return a match if either 1 OR the other are met. 

For example a|b with match if either condition "a" or "b" are met. 

### Character Classes

A character class is a set of characters that are enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string. 
For example, our code has the following snippet: 
[a-z0-9_\.-]

This means that any character between a-z, 0-9, _, -, . will return a match. 

### Flags

A flag is denoted by a lowercase letter and will give more guidelines for matching the string. The common letters are:

- i - which means ignore casing. This one make the expression non case-sensitive. 
- g - which means global. This searches for all occurences of the string, not just the first. 
- m - which means multiline. This will search line-by-line instead of the entire string. 

### Grouping and Capturing

Grouping and capturing are ways to search for a set of characters together. In our example we have the following snippet:
([a-z0-9_\.-]+)
This is the first group that is in our example, as denoted by the parentheses. It checks groups sequentially, so this group must be true before it checks the next groups.
The next groups in our example are:
([\da-z\.-]+) after the @ sign and ([a-z\.]{2,6})

### Bracket Expressions

Bracket expressions are a way to define a character class and specify a range of characters that can match a single character. They are enclosed in square brackets. For example, if I were to write [a-j], any letter between/including a through j will match. 
In our code, [a-z0-9_\.-]+ means that any letter/number/symbol contained in those brackets will return a match as long as there's at least one. 

### Greedy and Lazy Match

Greedy and lazy matches are terms to describe how the quantifiers should match patterns in the input text. A greedy quantifier will match as much as the input as possible. There are a couple of ways to denote a greedy quantifier including: *, +, and ?.
A lazy quantifier is denoted using the ? symbol and says to match as little of the input text as possible. 

### Boundaries

Boundaries are used to specify the location of a match between the code and the input text. We already talked about the ^ (start) and $ (end) boundaries. There is also \b, which signifies a position at the beginning or end of a word. 

### Back-references

A back-reference is something that allows you to match the same characters that were already grouped/captured earlier in the same regex code. They are denoted using the code \n. n is the number of the group captured. So \1 represents the first group captured. 

### Look-ahead and Look-behind

Look-ahead and look-behind say that specific conditions have to be met before or after the position in the input text. If the code says X(?=Y), than the current position matches X only if it followed by Y. 

## Author

Tommy Henderson is a bootcamp student with edX. 
GitHub profile: https://github.com/tommy-henderson/
