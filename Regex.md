# Regex Tutorial (Regular Expressions)

What are Regular Expressions or Regex?
- They are used in various programming languages to discover a specified combination of characters.
- The programmer can use Regex to find any variation of a string matching a pattern.
- For example a database with many E-Mail addresses , in this case Regex pattern can be used in the search of 

`[any name]@[any domain].[any extension]` 

## Summary

In this Tutorial, a regex for matching an email address will be introduced. Here is a snippet of the regex:

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

A caret (`^`) anchor defines the begining of the string while the dollar sign (`$`) defines the end of the string.

### Quantifiers

A quantifier allows the system to identify how the number of occurrences of the preceding characters. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The plus `+` will match one or more of the preceding character. In this case it will attempt to match 

`[a-z0-9_\.-]`.

Two numbers with curly brackets

 `{2,6}` 
 
 will match from two to six from the previous character. In this case it will match 
 
 `[a-z\.]`.
 
  As further examples:
  
   `{2}` 
   
   would match exactly two, and 
   
   `{2,}` 
   
   would match two or more.

### OR Operator

The pipe `|` matches the expression before or after it. This quantifier is affective for specific characters, or a whole expression.

### Character Classes

A character class will match one out of several characters and are often, but not exclusively, used in conjunction with bracket expressions.

`a-z` : Matches a character included between the two characters separated by the hyphen. 

In this example `a-z` will match any character between a and z.

`0-9` : matches any character between zero and nine.

`_` : Matches literal underscores. |

`\.` : Matches literals dot (.). Dots have special functions in regex. The backslash (\) is used to escape the character.

`-` : Matches literal hyphens.

`\d` : Matches any number

`@` : Match literal at signs. Found following the first parenthetical group in the email Regular Expressions.

### Flags

Flags will always follow the closing forward slash of an expression, and change how it is interpreted.

### Grouping and Capturing

Grouping allow a group of characters to be combined to operate on them together.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Capturing group `(ABC)` groups multiple characters together for extracting a substring.

This example has three capturing groups: 

`([a-z0-9_\.-]+)`, 

`([\da-z\.-]+)`, 

`([a-z\.]{2,6})`. 

This allows for a substring to be verified before `@`, another one before `\.`, and the final one for the domain extension of the email address.

### Bracket Expressions

This example has three groups of bracket expressions. Simply put, a bracket expression contains a list of characters enclosed in brackets: 

 ( [ & ] ). 
 
 This will perform a search of any characters found within this list. If the bracket expression begins with a caret (^), then the search will exclude all characters from that list.

### Greedy and Lazy Match

Quantifers can be either greedy or lazy. 

A greedy quantifer will attempt to match as many characters as possible as it goes backwards through the regex string. 

A lazy quantifier will attempt to match as few characters as possible as it goes back through the regex string. 

By default, quantifiers are greedy unless affected by another quantifier.

### Boundaries

The \b is an anchor like the caret and the dollar sign.

It matches at a position that is called a “word boundary”. Characters that are matched by the short-hand character class \w are the characters that are treated as word characters by word boundaries.

### Back-references

Back-references match the same text as previously matched by a capturing group.

### Look-ahead and Look-behind

Lookbehinds are specific for groups that are before the pattern.

Lookaheads are for groups after the pattern.

## Author

Nemo the Full-Stack Web Developer, to view more of his work please visit [GitHub](https://github.com/chunngaimo).