# Regex Tutorial

A regex (regular expression) is a sequence of characters that defines a specific search pattern.  When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are frequently used to validate input.

## Summary

The following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain. I'll break down those components and explain what they do.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors identify the positions of characters.  ^ and $

The caret `^` defines the beginning of the string.

The dollar sign `$` defines the end of the string.

### Quantifiers
A repitition operator. Quantifiers let the system know to match the preceding token a set number of times.

Quantifiers in this regex: the `+` operator. It connects the users email name + email service + .com. Another quantifier for this regex, `{2,6}`, will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping and Capturing
Capturing group #1 in this expression is `([a-z0-9_\.-]+)`. It matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the .com.

### Bracket Expressions 
Used to create a character set for matching each section.
Bracket expressions for email validation include the character sets of:

 * `[a-z0-9_\.-]`  

 `a-z` matches a character in this range and is case senstive. 

 `0-9` matches a character in this range and is case senstive.

 `_\.-` matches the characters "_", ".", and "-"

 
 * `[\da-z\.-]` 

 `\d` matches a single digit from 0-9

 `a-z` matches a character in this range and is case senstive.

 `\.-`  and the characters "." and "-".

 
 * `[a-z\.]` 

 `a-z` matches a character in this range and is case senstive. 

 `\.` matches the character ".".
 

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the + Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6}` for the last capture group.

## Author

Pamela Cleveland

[github](https://github.com/pamelac21)
