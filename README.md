# Regex Tutorial URL Validation

 Regex, or Regular Expression Syntax, is a useful tool for any web developer. Regular Expressions define a search pattern and are very useful for form input validation, web scraping, and filtering information. Creating a Gist allows the user to save code snippets or functions and recall or share them with others. This is a important tool to web development. It is important to remember when we discuss a string that we remember:

* The string can contain any lowercase letter between a–z

* The string can contain any number between 0–9

* The string can contain an underscore or hyphen

* The string is between 3–16 characters long

## Summary

In This Gist, Regex used for matching a URL will be discussed in this file. By implementing Regex the to match the URL the user can make sure that all the components of the URL are present when coding. Below is the expression for matching a URL.


```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```
  
## Table of Contents

- [Regex Tutorial URL Validation](#regex-tutorial-url-validation)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

A Regex is considered a literal, so the pattern must be wrapped in slash characters ```/```. In this gist we will look at the "Matching of a URL" as you can see it follows this pattern in the matching the URL below.

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

This does not say whether or not the URL is operational but rather is checking the string to make sure that components that make up a URL are in the string. This can help provide a needed check and balance for correct URL structure but does not give any indication that the URL is indeed functional. 

/```^```(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?```$```/

### Anchors

The characters ```^``` and ```$``` are both considered to be anchors. Anchors are placed at the beginning and end of each expression. The ```^``` character indicates that the string begins immediately following the character. The ```$``` character indicates that the string ends with the character immediately before it. You can see this implemented in the Matching the URL below.

/```^```(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?```$```/

### Quantifiers

Quantifiers are important for Regex Expressions because they count how many times a character, group, or class must be present for a match to be found. In the Match URL there are several different quantifiers in the expression.

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/```

The first quantifier in this expression is the ```?``` character in /^(https```?```:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

* The ```?``` matches the pattern zero or one time. This quantifier is preceeded by the ```s```. This means that the URL can begin with either ```http``` or ```https``` but not ```httf```.
  
The next quantifier is again a ```?``` but this time follows a group of characters  in parentheses.
/^(https?:\/\/)```?```([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

* Because of the different placement this will validate the group of characters inside the parenthesis. This will match zero to one times, meaning again that ```http```  ```https``` are both valid.
```https://www.al.com``` and ```al.com``` would both match this criteria.

The next quantifier in the match URL is the ```+```. In the match URL,  /^(https?:\/\/)?([\da-z\.-]```+```)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

* The ```+``` matches one or more times. This means that the item preceeding it must occur atleast once but can occur an infinite amount of time. The preceeding item is the following ```[\da-z\.]``` which means the match will work for any given string between the ```https://``` and the last ```.``` before ```com```

The curly bracket quantifier seen as the ```{2,6}``` in this expression matches the amount of times within the bracket. The comma in the middle signifies it will match an amount of times between the two numbers. In the match URL, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]```{2,6}```)([\/\w \.-]*)*\/?$/. This means it will match between 2 and 6 times. In addition the domain must be between 2 and 6 characters. ```.com```, ```.io```, ```.gov``` ```.edu``` would all qualify for this.

The final quantifier in the match URL expression is the ```*```. As seen here, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]```*```)```*```\/?$/. The ```*``` will match zero or more times and preceeding the first ```*``` is ```[\/\w \.-]``` which means it will match any length string after the ```.com```, ```.edu```, etc. It can be blank or extremely long.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

* This Regex tutorial was created by Brent Graves.

* Github Username:grave019
  
* [Brent Graves Github Profile](https://github.com/grave019)