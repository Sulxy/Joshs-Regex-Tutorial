# Understanding and Explaining the Regular Expression for Matching URLs 

Have you ever wondered how websites check for a valid web addres? They use regular expressions for this, which are basically just fancy search patterns. In this guide, we will break down the URL regex, which is specifically built to recognize URLs. This guide will take you step-by-step, and explain how each part of the URL regex works, and how to spot different types of URLs yourself.  

## Summary

Going forward, we will go over the make up of each component that creates a readable URL: Anchors, Quantifiers, OR Operator, CHaracter C Lasses, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy March, Boundaries, Back-references, and Look-ahead/Look-behind assertions. 

## Table of Contents

- [Regex Components](#regex-components)
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

The URL regex is made up of the following components:(/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/)

### Anchors

Anchors are like bookends -- they mark the beginning and end of a regex's search within a string. In the case of URLs, the (^) marks the start of the string, and the ($) marks the end. Essentially, we are telling the web adress to start looking at ^, and stop looking at $; The string inbetween is the relevant component. This helps to ensure that the entire string is looked at for a match against the defined pattern. This anchoring mechanism is crucial for precicely identiftying URLs within a large body of text, and providing results without overlooking any part of the URL. 

### Quantifiers

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
