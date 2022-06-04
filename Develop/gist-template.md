# Title (replace with your title)

<!-- Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ -->

Introductory paragraph (replace this with your text)

This is a tutorial to explain what a Regex (Regular Expression) is. In this tutorial I willl break down a regex part by part to explain what it means and how it works.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

The regex I have chosen is:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This regex is for matching an Emai address.

A regex is a sequence of characters that specifies a search pattern in text. They can be used for input validation. Each character has a specific meaning.

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

Some basic components of a Regex includes: character classes, flags, OR operator, quantifiers, anchors, boundaries, back-references, grouping and capturing, bracket expressions, greedy and lazy match, look-ahead and look-behind.

### Anchors

Anchors do not match a character and insread they match a position before, after, or between characters.

Examples:
\Z - End of string
\b - Word boundary
\B - Not word boundary
\< - Start of word
\> - End of word

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

Examples:

- 0 or more {3} Exactly 3

* 1 or more {3,} 3 or more
  ? 0 or 1 {3,5} 3, 4 or 5

### OR Operator

The OR operator can be used to match characters or expression of either the left or right of the | operator.

Examples:
(a|b) - a or b
[abc] - Range (a or b or c)

### Character Classes

A character class matches only a single character, can be used to match only one out of several characters.

Examples:
\c - Control character
\s - White space
\S - Not white space
\d - Digit

### Flags

Flags are optional parameters that can be added to a plain expression to make it search differently.

Examples:
i - Insensitive, makes the entire expression case-insensitive
m - Multi-line, when enabled the Anchors (^ $) will match the start and end of a line, rather than the whole string
g - Global, does not return after the first match, which restarted any subsequest searches from the end of the previous match (Makes the expression search for all occurences)

### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses.

Examples:

(abc){3} - matches abcabcabc. First group matches abc.
() - parentheses creates a capture group
(?<>) - using `?<>` puts a name to the group
(?:) - using `?:` disables the capturing group

### Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.

Examples:

'elephant'.match(/[abcd]/) // -> matches 'a'
'donkey'.match(/[^abcd]/) // -> matches 'o'

### Greedy and Lazy Match

Greedy search — will try to match the longest possible string.
Lazy Search — will try to match the smallest possible string.

Examples:
the greedy h.+l matches 'hell' in 'hello'
lazy h.+?l matches 'hel'

### Boundaries

Boundaries are characters that are helpful in 'anchoring' your pattern to some edge, but do not select any characters themselves. It matches at a position that is called a “word boundary”. This match is zero-length. 3 positions that qualify as word boundaries - Before the first character in the string, if the first character is a word character.
After the last character in the string, if the last character is a word character.
Between two characters in the string, where one is a word character and the other is not a word character.

Examples:
\b - word boundaries (as defined as any edge between a \w and \W )
\B - non-word-boundaries
^ - the beginning of the line
$ - the end of the line

### Back-references

A backreference in a regular expression identifies a previously matched group and looks for exactly the same text again. A simple example of the use of backreferences is when you wish to look for adjacent, repeated words in some text. The first part of the match could use a pattern that extracts a single word.

Examples:
([a-c])x\1x\1 matches axaxa, bxbxb and cxcxc

### Look-ahead and Look-behind

A positive lookahead (?=123) asserts the text is followed by the given pattern, without including the pattern in the match. Similarly, a positive lookbehind (?<=123) asserts the text is preceded by the given pattern. Replacing the = with ! negates the assertion.

Examples:
Input: 123456

123(?=456) - matches 123 (positive lookahead)
(?<=123)456 - matches 456 (positive lookbehind)
123(?!456) - fails (negative lookahead)
(?<!123)456 - fails (negative lookbehind)

## Author

This was a short project used to teach myself the basics of what regex expressions are and to accurately teach others like myself. If you have any questions please feel free to contact me at aniyah_mb@yahoo.com or visit my github profile to see more of my work. https://github.com/aniyahmb99

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
