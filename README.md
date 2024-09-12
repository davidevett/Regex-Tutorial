# Regex and You!

This project will be covering the details of Regex (or regular expression) and its its practical uses used today. 

## Summary

Regex short for regular expressions is very similar to an expression. For example a expression is a line of code that evaluates a value. this can be as simple as 2 + 2 = 4 or a complex combinations ov values function calls and other expressions. Regex however is a coloection of character that defines a pattern for searching and matching characters and sequence of characters.

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

Anchors are used to define the location of the pattern of characters. For example the caret (^) character specifies to look at the beginning of a string. If we searched for /^a/ in the string "abcdef" (a) would return. However, if we search the string "fdwagd" nothing would return. The antithesis to this character is the dollar sign ($) which specifies the end of a string. There are other anchors to be used but these are the 2 most common.

### Quantifiers

Quantifiers are used to define how many characters should be matched. The star (*) specifies zero or more matches. For example if we search /c*/ in the strings "asdccccc" "asdc" 'asdfcc" the would all return a value. Alternatively the plus (+) symbol specifies one additional element. So if we use /c+/ to search the strings "asdcc" the values "cc" would return. This symbol can be stacked appon to return additional elements. THe question (?) symbol specifies zero or one element. For example if we search /as?d/ in the strings "asd" "ad" it would return "asd" and "ad".

Specific Quantifiers can be used to define the number of characters that should be matched.

- {n} specifies the number of characters to be matched
- {n,} specifies a minimum number of characters to be matched
- {n,m} specifies a minimum and maximum number of character to be matched


### Grouping Constructs

Grouping constructs are methods that can be used to simplify complex code by finding repeated sequences in long strings dividing them into subexpressions. Common grouping constructs are:

- ( example ) This matches any group or instance of the characters within the parentheses 
- (?: example ) This is a noncapturing group that matches any character within the parentheses but does not capture the string.
- (?<name> example ) This creates a group and gives it a name to be called upon later.
- \k<name> This calls upon a named group

### Bracket Expressions

Bracket Expressions use brackets [] define a set of characters to match or unmatch. Using the brackets we can searach for instances of [asdf] in the string "asdff asdfasdf asf asdffffdf". Alternatively, you can use the caret character to unmatch the characters in the string. For example, [^asdf] will avoid all instances of "asdf" in the string. You can use this to filter down searches say if you were trying to ensure that a user would not be allowed to use any numbers in thier password. simply apply [^0-9] which will refuse and numbers from being recognized.

### Character Classes

In tandum with square brackets Character Classes or charcter set defines a range of characters to be matched. For example if we search /b[ae]t/ you could match "bat" or "bet". This can extend to any range of characters. For example [0-9], [a-z], and [A-Z] are valid character ranges used often in password or username matching.

### The OR Operator

The OR operator is intuitive and simply offers the ability to match one character or another. For example if is search for /abc|def/
in a string it will return "abc" or "def". This is generally used to search one group or another in a long string.

### Flags

Flags alter the behaviour of the regex to a desired paramater. For example:

- (i) Ignores casing in the string so that if the cat and Cat are bother returned in the search /Cat/.
- (g) Global flags match all occurrences of a pattern. If not specified than the first pattern will be matched.
- (m) If there are multiple lines of strings. The multiline (m) flag allows for searches to extend to the next line in the string. otherwise the search will only match the first line.
- (s) This allows a dot (.) to match allong a new line in the string.

### Character Escapes

Character Escapes target sets of characters to allow quickly targeting groups of characters. For example:

- (\d) Targets any number in the string.
- (\w) Targets characters [A-Z,a-z] numbers [0-9] or an underscore (_).
- (\s) Targets a space or a line terminator.

## Author

The author of this article was David Evett. Here is a link to my github to check out some of my work!

https://github.com/davidevett
