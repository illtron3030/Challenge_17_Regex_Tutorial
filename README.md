# # Regex Tutorial: Matching An Email
Regular expressions (Regex) are patterns used to match character combinations in strings. This tutorial explains the email regex by breaking down each part of the expression.

## Summary
The following expression can be used to verify that user input is a valid email address:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/i
```
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
Anchors are used to “anchor” the regex match at a certain position.
`^` matches the position before the first character in the string from the email, and `$` matches right after the last character in the string.

### Quantifiers
Quantifiers indicate numbers of characters or expressions to match. 
`{}` is the quantifiers in this expressrion. 
`{2,6}` here means to check if the eamil domain `.xx` has 2 to 6 letters.

### OR Operator
OR Operator `|` indicates the logical "or".
It doesn't have one here but you will use it in building a logical “or” operation using regular expressions.

### Character Classes
Character classes distinguish between various characters, such as letters and numbers.
`.` usually comes with `\`, otherwise it repsents a wildcard character.
`\d` is shorthand for digit 0 to 9.

### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. 
`i` makes the whole expression case-insensitive: no difference between A and a.

### Grouping and Capturing
Grouping and capturing `()` indicates groups of expression characters. 
`([a-z\.]{2,6})` here creates a capturing group with both `[a-z\.]` and `{2,6}`.

### Bracket Expressions
Bracket Expressions `[]` can match any values you put inside the `[]`.
`[a-z0-9_\.-]` here can match with characters`a-z`, numbers`0-9` or symbols `_` `.` `-` that typically used in the email address.

### Greedy and Lazy Match
The quantifiers ` * + {}` are greedy operators, so they expand the match as far as they can through the provided text.
`\da-z\.-]+` can match with any numbers, characters, and symbol`.` or `-`.
Lazy Match `?` means to match the shortest possible string. By adding the `?` after the `* + {}`, we tell it to repeat as few times as possible.
### Boundaries
Boundaries`\b` represents an anchor matching positions where one side is a word character, and the other side is not a word character. It performs a "whole words only" search.

### Back-references
Back-reference `\1` refers to a previous part of the matched regular expression.

### Look-ahead and Look-behind
If we want to find matches for a pattern that are followed or preceded by another pattern, it's called “lookahead” and “lookbehind”.

## Author

Ilya Feldman, Aquarius. <br>(replace with your information and a link to your profile)
