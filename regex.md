# Matching a URL

This Regex will be explaining the componenants of matching URL values using regular expressions through Javascript.

## Summary
First of all what is A Regex(regular expression)? 
A Regex or regular expression is a sequence of charaters that defines a search pattern in a body of text, Regexs are utilized in search engines, word proccesors and text editors.They are also frequently used to validate an input such as a user enetering an email adress.
In this Regex Tutuorial we will be going over the components of matching URL values using regular expressions. Below is an example of the Regex we will be looking at:
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
This string of characters may look like nonsense but serves a very improtant role, this regex basically asks if an inputed URL is valid. While it can have lots of different applications it is most commonly used in input data verifacation.
Follow on down below to pull this Regex apart and see how it works.

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
Lets start breaking down this Regex to understand what is happening.

### Anchors
The two Anchors in our example Regex are the Caret Anchor ^ and the dollar sign Anchor $.
What do these Anchors do?
The Caret Anchor ^ marks the beginning of the regex text while the dollar sign Anchor $ denotes the end of the Regex text, together they amount to an exact string match with the components between the two Anchors.
By wrapping the Regex between The Caret ^ and dollar sign $ Anchor the search function is asked to match exactly what is inside of them.

### Quantifiers
What are Quantifiers?
Quantifers specify how many times a character, group, or character classes must be used inside of an input to find a match.
In our Regex example the following quantifiers can be found *,+,? and {}.

The * quantifier matches the character element zero or more times.

The + quantifier means one or more where more can actually mean unlimited times, in regards to our Regex example it located in the second capture group  after the character set. What this means for this specfific portion of the regex is that it is searching for specified characters in the set and requires them to be there to make a match.

The ? quantifier does the opposite of the + quantifier, so the ? Quantifier matches one or less this essentailly means the character, group or character class is optional. However the regex will still search for it if it is there.

The {} quantifier defines a range of instances where a match can be identified, in our Regex example we can see {2,6}, therefore our range quantifier allows the regex to match a group of characters between two and six characters.
This would translate to the top level domain of a URL for example .com, .au .gov etc etc. Why this range has been given is becasue a majority of top level domains are between two and six characters in length.

### Grouping Constructs
Grouping inside of a Regex is done with Parenthesis(), in our example Regex multiple parts have been grouped:
(https?:\/\/)
([\da-z\.-]+)
([a-z\.]{2,6})
([\/\w \.-]*)
When Specific parts of a Regex are grouped it allows us to a apply a quantifier to the targeted group, when parts of the Regex are grouped it creates a Captured group.

### Bracket Expressions
Bracket expressions are characters enclosed inside of square brackets[].
Bracket expressions include specific characters that will only match with the parts of an input that contain specified charaters inside the brackets.
For example:
[gevq] an input matching parts of these characters will match.
We see this in our example Regex here [\da-z\.-], [\/\w \.-].

### Character Classes
The character classes shown in or example Regex are the \d character class and the \w character class.
The \d character class looks for any digit in the Regex while the \w character class looks for any alphanumeric character.
Character classes are notations that match any symbol from a predetermined set, using these character classes will match characters within there defintions.

### The OR Operator
The or operator | is used to match the characters to right or left side of the operator, our example Regex does not feature a or operator.

### Flags
Regexs can have flags that that define additional functionality or limits for the regex, our example regex does not have any flags, but some exaples include:
g for global search
i for a case senstive search
m for multi line search

### Character Escapes
A character escape \ escapes a character that would be interpretaded literally, if a character escape was before curly braces{} that would mean the regex would look for the curly braces instead of trying to define a quantifier. Character escapes lose there significane inside of bracket expressions.

## Author

This Regex was created by Zachary Smart

Github: https://github.com/Zac0088