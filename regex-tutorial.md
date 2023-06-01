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

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
