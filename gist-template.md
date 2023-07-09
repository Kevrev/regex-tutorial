# Regex Tutorial - Matching an Email

Regular expressions provide developers with a strong asset in being able to target specific patterns within a string. This particular tutorial is focused on a regex that matches with an email. We will explore each component of the regex and the purpose they serve, which also gives insight on how they are utilitzed in a broader sense.

## Summary

This regex tutorial specificially pertains to the expression used to match email. Email matching can be used to validate that a user has entered a valid email address. This can be useful for a ensuring that a user has entered a valid email address when signing up for a website. 

The regular expression is as follows: 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

`^` and `$` are the anchors used in this regex. `^` indicates that the pattern we are looking for should be at the start of a string, and `$` indicates that the pattern should be at the end of a string. Used in conjunction with one another, it can specifically isolate the email by itself such as `test@email.com` rather than `My email is test@email.com by the way`.


### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers can be used to enforce limits or ensure that some portion of the regex appears a designated number of times, or less than a designated number of times. In this case, `+` is used to ensure that the preceding character set appears at least once (ensuring no empty string), but does set a strict limit. This is used to ensure that the email address has at least one character before the `@` symbol (`test`), and at least one character after the `@` symbol (`email`), giving you `test@email` with the final portion being next. 

The case {2,6} is determining the allowed length on the last portion of an email address (`.com`, `.net`, `.org`, `.co.uk` etc.). As there are currently no one letter TLDs, it prevents things like `.c` from being accepted as a valid email address, but a length of 6 may also be short as it can prevent things like `.outlook` or `.hotmail` from being accepted as a valid email address.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
