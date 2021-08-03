# Regex Tutorial

Regex is a sequence of characters that are used in specific search patterns. Regex is a shortcut for regular expressions and throughout this gist i will be explaining what each part of it is.

## Summary

Throughout this gist Regex will be explained and simplified for you to understand the concept and ideas behind it. 

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

## Regex Components Include

### Anchors
Anchors help define a search from beginning to end.

According to the documentation /^ and $/ are indicators that the expression is either beginning or ending.

- This ^ initiates the beginning of the string and could also mean the beginning of the line if (m) or the multiline flags are enabled. This matches a new position not a single character. 

- Like the ^ the $ indicates the end of the string or the end of a line if (m) or the multiline flags are enabled. Which also matches a new position and not a single character. 

### Quantifiers

- Quantifiers are things that tell you how many times certain parts of your expressions should be repeated.

### OR Operator

- OR Operator also known as || acts as a boolean or also matches the expression or expressions before or after the ||. The patterns get tested in order, it checks any two operands that are non-zero (0, undefined, false, NULL and "" which is also considered a zero.) It can operate within groups or whole expressions. 

### Character Classes

Character Classes match characters to a specific set. There are numbers of predefined character classes but you're also able to define your own sets. 

### Flags

Interpreted Expressions can be changed through Expression Flags, flags are followed by the closing forward slash of the expression. The 6 different types will be listed below. 

- "i" this means to ignore the case so it Doesn't matteer between UPPERCASE and lowercase

- "g" This is a (global) flag search retains index of the last match. This allows subsequent searches from beginning to end of the previous matches. Without the global flag, each one returns the same match.

- "m" this is a multiline flag and when it is enabled the beggining and end anchors will match with the beginning and end of a line instead of the whole string. 

- "u" The unicode flag will enable the handling of surrogate pairs

- "s" which enables dotall .mode which matches any characters including new lines

### Grouping and Capturing

(ABCD) () regular expressions allow us to not only match the text but also extract the info for further processing. This can be done by defining groups of characters and capturing them using parentheses and metacharacters. Sub-patterns inside parentheses will be captured as groups. This can be used to extract information and all types of data such as emails and phone numbers.

### Bracket Expressions

Bracket Expressions are enclosed in square brackets which also matches a single character and or ordered elements. Initial characters are circumflex ^, then the bracket expression is complemented

### Greedy and Lazy Match

The behavior Greedy means that you match the longest possible string. Greedy quantifiers tells the engine to match as many possible instances of it's quantified token or sub-pattern as possible. 

The Behaviour Lazy is essentially the opposite which is matching the shortest possible string and to match the fewest amount of quantified tokens as needed. The table below indicates a regular quantifier and is made lazy by a "?" being appended to it. 

### Boundaries

"\b" is an anchor similiar to the ^ and $. The position is called a word boundary. It is a zero-length match. Characters that are matched by the short-hand character class \w are the characters that are treated as word characters by word boundaries.

Since digits are considered to be word characters, \b5\b can be used to match a 5 that is not part of a larger number. Putting a \b before and after an alphanumeric sequence matches are more exact than putting it “before and after a word”.

\B is the negated version of \b. \B matches at every location where \b does not. Effectively, \B matches at any position between two word characters as well as at any position between two non-word characters. There are more boundaries with the regular expression. Some examples include POSIX, GNU and Tcl.
### Back-references

Backreferences match the same exact text as previously matched by a capturing group. Let’s just say you want to match a pair of opening and closing <HTML> tags as well as the text in between. By putting the opening tag into backreferences, we can reuse the name or names of the tags for the closing tag.

Examples Include: 

<([A-Z][0-9])\b[^>]>.?</\1> This regular expression contains only one pair of parentheses, which capture the string matched by [A-Z][0-9]. The opening <HTML> tag. The backreference \1 references the first capturing group and \1 matches the exact same text that was matched by the first capturing group. The / before all of it is a literal character. It is simply the forward slash in the closing <HTML> tag that we are attempting to match.

### Look-ahead and Look-behind

Lookahead and lookbehind in groups are called “lookaround”. They are zero-length declarations just like the begiining and end of a line, and start and end of the word anchors. There are positive and negative lookarounds.

## Author

My Name is David Sanchez and I'm an aspriring Full Stack Software Engineer that attended the University of Utah Coding BootCamp.

You can look me up in github through my username which is Dsanchezjr99 or through this link [ https://github.com/dsanchezjr99 ]