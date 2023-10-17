# Computer-Science-for-JavaScript-Regex-Tutorial
A brief, but detailed introduction to Regex
## Summary
Here's a JavaScript expression (regex) pattern that matches the email "javierburgara150@yahoo.com":/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
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
Before I start explaining regex in this anchors, regex pattern must be wrapped in slash characters `(/)` as seen in our regex example.
### Anchors
The anchors used in this regex expression for matching an email are `^` , which indicates the beginning of the string and `$` to indicate the ending of the string.
### Quantifiers
Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com. 
Another quantifier for this regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.
### Grouping Constructs
Capturing group #1 in this expression is ([a-z0-9_\.-]+) that matches the user email name. The second capturing group is ([\da-z\.-]+) which will match the email service. Then lastly, capture group #3 is ([a-z\.]{2,6}) to capture the .com.
### Bracket Expressions
`[a-zA-Z0-9._-]`: Matches a single character that is either an uppercase letter (A-Z), lowercase letter (a-z), digit (0-9), period (.), underscore (_), or hyphen (-). It allows these characters in the local part of the email.
`[a-zA-Z0-9.-]`: Matches a single character that is either an uppercase letter (A-Z), lowercase letter (a-z), digit (0-9), period (.), or hyphen (-). It allows these characters in the domain name.
`[a-zA-Z]`: Matches a single alphabetic character. It ensures that the TLD consists of at least two letters.
### Character Classes
The character class in this expression is `\d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44".
### The OR Operator
`| and []`
`x(y|z)` matches a string that has x followed by y or z; captures y and z, this will be explained later xy or xz but not xyz
`x[yz]` same as above but it does not capture y or z xy or xz but not xyz
### Flags
Flags modify the behavior of the regex pattern, such as case-insensitive matching (i flag), global matching (g flag), or multiline matching (m flag). 
Like the OR Operator, no flags are specified in this regex.
### Character Classes
`\`. (escaped period): Matches a literal period. It is used to match the dot in the domain name.
### Bracket Expressions
Bracked expressios for email validation includes the character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z\.-], which is matching a single digit from 0-9, any character a-z (case senstive).
### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the + Quantifier, it will match as many times as possible giving back as needed. 
Another greedy Quantifier used in this regex is {} when matching `{2,6} for the last capture group.
### Boundaries
How to set boundaries in regex?
Boundary markers such as ^ and $ allow you to anchor the regex pattern to the beginning and end of the line (or string depending on which flags you use) respectively.
## Author
Made by Javier Burgara, a student at UCSD Extended Studies amd lover of code and video games. https://github.com/JavierBurgara

