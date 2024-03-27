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

Quantifiers in regex's determine how many times a character or a group of characters can appear in the input string. In this case, we have 3 different types of quantifiers that help create varying types of URLs:

    Optional Quantifier (?): The (?) in the regex says that the previous character or group of characters is optional. For example: (https?:) in this case, the '?' is saying that the 's' is optional, which allows the URL to have either (http://) or (https://).

    One of More Quantifier (+): The (+) symbol marks that the previous character or group of characters must appear at least once, but could appear many times. For example: [\da-z\.-]+ is saying that a digit, lowercase letter, period, or hyphen, must occur. 

    Zero or More Quantifier(*): The (*) symbol means that the previous character or group of characters must appear zero or more times. This helps to allow for flexibility in the URL while still being valid. For example: ([\/\w \.-]*)* says that a path component for the URL can have any combination of slashes, word characters, dots, spaces, hyphens, or even be empty. 

These quantifiers allow the regex to be adaptable to many different URL formats. If a component is required, optional, or can appear multiple times, the quantifers help make sure that the regex can capture the structure of the URL. This level of flexibility is mandatory for real-world scenarios where the URLs can vary in length, make up, and complexity. 

### OR Operator

This operator is represented by ([ and ]). It allows us to have multiple alternatives within a regex. Inside the URL regex (pasted again for convienence  (/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/)) the OR operator is structured to imply alternatives.

    Examples:
        [\da-z\.-]+: This matches a domain name, where a range of characters is accepted: digits, lowercase letters, periods, and hyphens. The 'd' is for digits, 'a-z' is the entirety of the lowercase alphabet. This criteria is opened and closed with a '\'. Then the '.' and '-' are for allowing the use of '.' and '-'. The whole thing is wrapped in []'s.  

        \.([a-z\.]{2,6}): The '[a-z\.]' allows for lowercase letters and periods '.'. The {2,6} specifies that the TLD (Top-Level Domain) has to be between 2 and 6 characters long. The TLD (.com, .org, etc) comes after the domain name. 

This kind of URL structure allows for alternatives within sections of the URL, and allows the for flexibility without having to list out every possible scenario. 

### Character Classes

Character classes can be explained by creating two camps: 

    Camp 1: [\da-z\.-]: This camp is open to digits (d), lowercase letters (a-z), periods (.), and hyphens (-). 
    Camp 2: [a-z\.]: This camp is open to lowercase letters (a-z), and periods (.). 

These camps help the regex understand which characters are allowed in a certain part of a URL. When the regex is looking through a URL, it now knows which characters are okay in which section of a URL, and which ones are not allowed. There are more character classes than what I used in the example above. The rest of them are detailed below: 

    /: allows the use of a forward slash.
    \w: allows the use of any word character. 

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
