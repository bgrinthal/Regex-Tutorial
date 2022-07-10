# Regex - Matching a URL

Developers write code, but they also *write about code*. Where I will be writing about a specific regex or regular expression.  This is a string of text that allows you to create patterns that help match, locate or manage text.  These are frequently used to validate input.

## Summary

Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

The regex above can be used to validate a URL.  I will be breaking it down into its components listed in the tabe of contents.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

All regex start and end with "/" followed by the anchors to begin and terminate the string.
The "^" anchor signifies the beginning for the regex string while the & achnor signifies the end.

### Quantifiers

( * ) - Matches zero or more times
( + ) - Matches one or more times
( ? ) - Matches zero or one times
( { n } ) - Matches exactly n times
( { n, } ) - Matches at least n times
( {n , m} ) - Matches from n to m times

Looking at our regex we will point out some qualifiers:

https? - it will look for this patterns 0 to 1 times based on the ( ? )
[a-z\.]{2,6} - it is looking for a matching paterns of [a-z\.] between 2 to 6 times
[\/\w \.-]* - it is looking for a matching patterns of [\/\w \.-] zero or more times

### Grouping Constructs

This is done by using parenthasis "()" to create sections or subexpressions.  This can be used to match a subexpression that is repeated in the input string.

`(https?:\/\/) ([\da-z\.-]+) [a-z\.]{2,6}) ([\/\w \.-]*)`

I removed additional code to show each of the 4 sections clearly.

### Bracket Expressions

Brackets "[]" indicate a set of characters to match.  This range of characters is called a bracket expression.

`[\da-z\.-]  [a-z\.]  [\/\w \.-]`

I removed addional code to show each of the 3 bracket expressions more clearly.

[a-z] - The string can contain any lowercase letter between a-z.
[a-z\.] - matches a single character in the range between a-z with a character.
[\da-z\.-] - matches single character in the range between a-z before one digit equivalent to 0-9 and the characters . and -.
[\/\w \.-] - \/ matches the character / , \w mathes any word character equivalent to a-z, A-Z, or 0-9 ( [a-zA-Z0-9] ), \.- matches the character . and -

### Character Classes

Defines the kinds of characters such as destinguishing between letters and digits.  There are many character classes but below is a couple from the code we are using:

. - matches any character
\d - matches a singel character that is a digit
\w - maches any alphanumeric or underscore character

### The OR Operator

The OR Operator "|" broadens our search to match characters or expressions to either the left or the right of this operator.

There are nor OR operators in our code but for example (t|T) will match either t or T.

### Flags

Flags can be used to effect the search to make it more specific.  We do not have any flags in our regex but below are a list of a few:

d- generate indices for substring matches
g- global search
i- case-sensitive search
m- multi-line search
s- allows . to match newline characters

### Character Escapes

The "\" is known as the character escape code, which restores the original literal meaning of the following character.

## Author

Written by Benjamin Grinthal

GitHub Profile:
https://github.com/izzziej
