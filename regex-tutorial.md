# A RegEx Tutorial

This git gist will be walking you through a regex tutorial. Firstly, regex is an abbreviation for 'regualr expressions' which are a set of characters used to create patterns that are used to find, replace, validate or search for text throughout most languages. Within this tutorial we will be looking at a code snippet which is used for matching hexadecmial values.

## Summary

This tutorial will navigate you through the different components of a regex used to match hex codes. Hex codes are used to choose colours by using the hexadecimal format. Hex codes will always start with # and can be in a hex triplet or a shorthand hex format.

Hex Triplet Formats Include: #000000, #FFFFFFF
Shorthand Hex Format: #000, #FFF

The hex triplet format doubles the shorthand for example #000 > #000000 as a hex value is always 6 numbers after a #.

The regex we are using within this tutorial to match our hex values is:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The anchor refers to what starts and ends the regex therefore providing guidelines which need to be met in order to make the match. The anchors in this example are ^ (caret) and $ (dollar sign).

### Quantifiers

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

A quantifer allows the regex to specify how many instances of a character, group, or character class have to be present in order to make a match. For exmaple if we had abc+, this would match any string with ab followed by a minimum of one c. The + quantifier means that it has to contain at least one of these in order to match. Other types of quantifers are: ,+,?,{}. The ? indicates the expression to match 0 or 1 time.

As mentioned, our regex will look at the two types of hex value formats, this indicates that the length of the component preceding these quantifiers should be 6 for {6} and 3 for {3} which is used to match the triplet format and the shorthand format.

### Grouping Constructs

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Grouping constructs are used to create logical groups within a regex pattern. They allow you to apply quantifiers or other operations to a group of characters as a whole.

For example, ([a-f0-9]{6}|[a-f0-9]{3}) represents a group that matches either a 6-character hex code ([a-f0-9]{6}) or a 3-character hex code ([a-f0-9]{3}). This grouping construct allows us to specify the length alternatives for the hex code in a concise way and apply quantifiers or other operations to the entire group.

### Bracket Expressions

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Bracket expressions signify the beginning of a character class within a regex pattern. In our example, the bracket expression [a-f0-9] is used on both sides of the OR operator (|) to search for the same set of values. This character class matches lowercase letters a to f and digits 0 to 9.

([a-f0-9]{6}|[a-f0-9]{3})

### Character Classes

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Character classes are used within our snippet so our regex knows what characters to expect. Our example shows our character classes being defined between our square brackets []. In our example we are using [a-f0-9] either side of our OR operator to search for the same values. This class is created so that a-f searches for letters a-f and 0-9 searches for digits 0-9.

### The OR Operator

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The OR operator in our regex is defined using this | element. The OR operator indicates that we could match our values based on either of the components that we are sperating by using an OR / | operator. This means that our hex value could either be 6 characters [a-f0-9]{6} or 3 characters [a-f0-9]{3}.

### Flags

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Flags, are also known as modifiers and options. They are additional settings that can be applied to a regex pattern to change its behavior. These flags are usually placed at the end of the regex pattern. Common flags include i (case-insensitive matching), g (global matching), and m (multiline matching).

Hex values aren't case sensitive therefore we don't need to use a flag within our regex.

### Character Escapes

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Character escapes allow you to match characters that have special meanings or are difficult to include directly in a regex pattern. For example, to match a literal period (.) or square bracket ([), you would use the backslash (\) as an escape character. In our example, no character escapes are needed.

Character escapes are dependent on what requirements your regex has.

## Author

Faith Meades is studying to become a full stack web developer with the University Of Birmingham.

GitHub:
