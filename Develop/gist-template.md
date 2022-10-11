# Regex Tutorial Email

In this tutorial I will be discussing how to match an email based on a regex. A regex, also known as a regular expression, are a series of special characters that can be search within a specific string.

## Summary

As stated in my introduction this regex tutorial is going to describe how to match an email adress. An example of this code would be /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This is a search pattern for email validation. It searches for any lowercase letters between a-z, any number between 0-9, and includes an @ sign. It then goes on to look for a domain name with any lowercase letters through a-z. Following that it looks for any lowercase letter from a-z after the period which can be anywhere between 2 and 6 characters.

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

There are two anchors used throughout regex expressions. These two characters are the ^ and the $. The ^ anchor shows the beginning of the string and the $ anchor shows the end of a given string. The ^ anchor is located after the first slash in my code / and the $ anchor is located before the last / in my code.

### Quantifiers

The quantifier seen in this expression are the + sign and the curly brackets containing numbers. The + sign in my expression indicates that it must match at least one of the previous inputs, meaning that there must be at least one lowercase letter from a-z in the email and domain, or one number from 0-9 in the email. The second quantifier in our code indicates that the regex must match 2-6 characters after the domain name.

### OR Operator

In our email regex we do not currently utilize an OR operator. An OR operator is a | symbol that matches a character either before or after the | operator. For example a | b represents that a character could be either a or b.

### Character Classes

The \ symbol in regex escapes a character. In our email example the \ is used to separate the email name from the domain. In our example it will look for the period and thus the continuation of the domain name rather then the beginning of a new quantifier. The period character class after the \ which escapes the character matches any character except the newline character. Following on from this, the \d character class we have in our example matches any numerical value from 0-9.

### Flags

In our example there is currently no flag used in this email regex. However, flags can be found at the end of a regex after the second slash. These flags are g, i, m, s, and y. The g is a global search flag which means that the regex should be tested for all possible matches in a string. The i is a case-insensitive search flag which means that the case should be ignored when matching a string. The m is a multi-line search flag which describes how a multi-line string should be treated as multiple lines. The s is a dot-all flag which causes the period to match any character. Finally, the y is a sticky flag which will only match from the last index position.

### Grouping and Capturing

Typically in a regex groups are made by using parantheses. Because of this, we can see that there are three groups used in our email regex example. These are the email name, the host name, and finally the domain. The email name group is ([a-z0-9_\.-]+), the host name group is ([\da-z\.-]+), and the domain name group is ([a-z\.]{2,6}).

### Bracket Expressions

The brackets in a regex represents the range of characters that we want to match. As shown in our grouping and capturing chapter listed above, we once again see that there are three bracket expressions in our example. As before, the bracket expressions are our email name, host name, and domain name. These describe the a-z characters as well as the numbers used.

### Greedy and Lazy Match

A greedy match in a regex expression will link to the longest string possible. Opposing this, however, is the lazy match which will take the shortest route to meet the shortest string possible. In our example the \d is a greedy match because it will try and match as many digits as possible. An example of a laxy match, which is not included in our example is the ? quantifier which looks for zero to one matches.

### Boundaries

In a regex expression, \b is a boundary which defines what can be matched to the left and right of a given position. In our given example, we do not have any boundaries as we can see that there is no \b in the beginning of our code.

### Back-references

Back-references match the same text already matched by a different capturing group. We can do this by using the \n back-reference. In our given example, however, we also do not have any back-references as we cannot see a \n.

### Look-ahead and Look-behind

Though there are no look-aheads or look-behinds, also known as lookarounds, in our example these are assertions that are added to the beginning and ending of word expressions and/or lines. These lookarounds search for matches but do not bring them up.

## Author

Alyssa Gantos is currently a student at Vanderbilt's coding bootcamp. Below you will find a link to her Github which features a multitude of her other projects. Thank you for reading and enjoying this tutorial for an email regex!

[Alyssa's Github](https://github.com/aalissy)
