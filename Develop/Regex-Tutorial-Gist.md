# Regex Tutorial for Matching an Email

Regex or Regular Expression is a way to find any text or information by searching for specific search patterns and extracting that information from any text rather than using literal characters which will only help you find literally an exact copy of what your searching for. In this case we will be searching for patterns that match a users email and we want to find all existing emails within a document rather than just one we could find by searching for that literal email.

## Summary

* As stated above the focus of this gist is to understand how we would go about searching for emails within any text using Regex expressions and understanding what each component is responsible for in creating a Regex.
* The Regex for matching an Email would look as such.  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
* Lets go ahead and break this down by its components.

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

### Flags

Lets start with the Flags because they are the components in which the Regex is usually written inside of. The flags are represented by the forward slash or '/' key. As you can see our Regex for matching Emails is all held between two forward slashes.

### Anchors

The next component we see after the first forward slash is the Circumflex or the '^' key. This would symbolize an Anchor which is basically looking for what the Regex starts or ends with. In this case we have both the Circumflex and the Dollar sign or '$' key. If you take another look at our Regex for matching Emails you'll notice that the '^' is looking for anything that starts with ([a-z0-9_\.-]+) and ends with ([a-z\.]{2,6}). We will get to what those expressions mean in detail later on

### Bracket Expressions

You'll notice that we have a few cases where we see Brackets or '[]' keys. This is basically telling the computer to match anything within the brackets. You can put literal expressions withing these brackets but for our Regex we are using them to find any letters (case-sensitive) and any numbers that may be linked to an email. Ill use the first part of the Regex for an example. [a-z0-9_\.-] would be looking for any letters a-z any numbers 0-9 and any literal underscore period or dash if needed.

### Character Classes

This brings us to the next set of components and we will use the example '[\da-z\.-]' to explain. First we have \d which is telling us to match a single character that is a digit. Next would be '\.' which is telling us to match any character to that may be found for extraction. (There are also classes \w that matches a word character and \s which matches a whitespace character).

### Grouping and Capturing

By now im sure you've noticed we use parenthesis '()' on three separate occasions within our Regex and this simply means we have 3 different capturing groups that are focussed on matching what we need within them

### Quantifiers

Within our Regex we have a few quantifiers. The '+' would give us matches within the previous brackets followed by one or unlimited more tokens within brackets as needed. (also referred as a greedy match). Then we have the '{2,6}' quantifier that matches a string within the previous brackets and is followed by 2 up to 6 copies of the sequence. (also greedy).  Quantifiers can also be to match anything needed within parenthesis as well.

## Summary

To summarize what is going on when we use the Regex /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ for matching Emails. We are looking at three different groups within our flags that make up an email and within the groups we are looking for any possible matches that could be found within an Email. 

## Author

- Asa Grace

- Email: asag182@gmail.com

- GitHub: https://github.com/asa-grace