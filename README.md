# Regex-Tutorial for Matching an Email 

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

Below will be an summarize breakdown of the regex process of matching an email and which components were used for this partiular regex process using the regular expression:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Character Classes](#character-classes)
- [Quantifiers](#quantifiers)
- [Literal Character](#literal-characters)

## Regex Components


### Anchors
Purpose of Anchors is to define positions in a string where matches must occur, which are crucial for input validation and precise pattern matching.
Anchors can also be used multiple times in a pattern and combined with other regex elements.

Usage/Examples for Email:

`^`: Matches the start of a string or line.
- Example: /^([a-z0-9_\.-]+)

`$`: Matches the end of a string or line.
- Example: ([a-z\.]{2,6})$/


### Character Classes
Character classes allows a match for any single character that is either a letter lowercase or uppercase, a digit, or one of the speicified special characters defined by square brackets.

Usage/Examples for Email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

`[]` It specifies a set of characters to match.
- `a-z`: Matches any lowercase letter from 'a' to 'z'
- `A-Z`: Matches any uppercase letter from 'A' to 'Z'
- `0-9`: Matches any digit from '0' to '9'
- `._%+-`:  Matches these specific special characters literally


### Quantifiers
Quantifiers are metacharacters to quantify how many times a character, group, or character class should be matched in a pattern. 

Usage/Examples for Email:

- Example: `+` Matched one or more occurrences of the preceding element in this case would be the character class. 

Combinded Effect:
Together, `[a-z0-9_\.-]+` means:

"Match one or more characters, where each character can be any lowercase letter, uppercase letter, digit, or one of the special characters . _ + -"

This is particularly useful for matching the local part of an email address, as it allows for a wide range of valid characters while ensuring at least one character is present.

###  Literal Characters 
Literal characters in regular expressions are characters that match themselves exactly without any special meaning and match themselves exactly in the input text.

- Example: `@` Symbol and Single characters: `'a', 'b', '1', '2'`

Usage/Examples for Email:
`a-z, 0-9, @`

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


## Author
This tutorial was created by Erica with resources provided, click link to view GitHub [repo](https://github.com/Ejacosta86/Regex-Tutorial-).
